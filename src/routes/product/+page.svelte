<script>
	import { onMount } from "svelte";

	let cart = [];
    let total = 0;
    let products = [
    {
        id: 1,
        name: "Apple", 
        image: 'src/images/apple.png',
        harga: 10000,
        jumlah: 1
    },
    {
        id: 2,
        name: "Jeruk",
        image: 'src/images/orange.png',
        harga: 5000,
        jumlah: 1
        
    },
    {
        id: 3,
        name: "Strawberry", 
        image: 'src/images/strawberry.png', 
        harga: 8000,
        jumlah: 1
    }
]
 
const addToCart = (product) => {
    for (let item of cart){
        if(item.id === product.id ){
            product.jumlah += 1
            cart = cart;
            localStorage.setItem('items', JSON.stringify(cart));
            return;
        }
    }
	 cart = [...cart, product]

     //set to local storage
     localStorage.setItem('items', JSON.stringify(cart));
 }
 

const minusItem = (product) => {
    for (let item of cart){
        if(item.id === product.id ){
            product.jumlah -= 1
            cart = cart;
            localStorage.setItem('items', JSON.stringify(cart));
            return;
        }
    }
    cart = [...cart, product]
     //set to local storage
    localStorage.setItem('items', JSON.stringify(cart));
 }

const plusItem = (product) => {
  for (let item of cart){
        if(item.id === product.id ){
            product.jumlah += 1
            cart = cart;
            localStorage.setItem('items', JSON.stringify(cart));
            return;
        }
    }
	cart = [...cart, product]
     //set to local storage
    localStorage.setItem('items', JSON.stringify(cart));
 }

    onMount(function() {
        bugStorage();
    });

	function bugStorage() {
		if (typeof window !== "undefined") {
            const isReady = localStorage.getItem('items')
            if(isReady){
                const parse = JSON.parse(isReady);
                parse.map(function(val, key) {
                    if(val.jumlah > 0){
                        cart = [...cart, val]
                    }
                });
            }
		}
	}

$: {
    total = cart.reduce((sum, item) => sum + item.harga * item.jumlah, 0)
}
</script>



<h3>There are {cart.length} item in your cart</h3>

<div class="container">
        <div class="product-list">
            {#each products as product }
                <div class="image" style="background-image: url({product.image});">
                <div class="deskripsi">
                <h4>{product.name}</h4>
                <p>Rp {product.harga}</p>
		        <button class="btn-cart" on:click={() => addToCart(product)}>Add to Cart</button>
                </div>
                </div>
            {/each}
            
        </div>
        <div class="card-list">
            {#each cart as item}
            {#if item.jumlah > 0}
                <div class="cart-item">
                    <img width="50" src="{item.image}" alt="{item.name}">
                    <p>{item.jumlah}</p>
                    <button on:click={() => minusItem(item)}>-</button>
                    <button on:click={() => plusItem(item)}>+</button>
                    <p>{item.harga * item.jumlah}</p>
                </div>
                {/if}
            {/each}
            <div class="total">
               <h4>Total: {total}</h4>
            </div>
        </div>
</div>

<style>
    .deskripsi{
        margin-top: 110px;
    }
    .image{
        height: 100px;
        width:100px;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
    }

    .product-list {
        display: grid;
        grid-template-columns: repeat(3, 1fr );
        
    }
    .btn-cart{
        height: 50px;
        width: 100px;
        margin-bottom: -8px !important;
        border-radius: 20px;
        background-color: #e7c6a8;
        border: 0;
    }
    .btn-cart:hover{
        background-color: antiquewhite;
        cursor: pointer;
}
    
    .total {
        margin-top: 125px;
        text-align: right;
    }

    .product-list > div {
        padding: 10px 0;
        font-size: 20px;
    }
    .card-list {
        display: grid;
        grid-template-columns: repeat(3, 1fr );
    }
    .cart-item{
        margin-top: 210px;
    }
</style>
   