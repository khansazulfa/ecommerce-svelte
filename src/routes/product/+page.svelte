<script>
	import { cartProduct } from './../../stores/formStore.js';
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


    function addProduct(produk) {
        $cartProduct.push (produk);
        $cartProduct = $cartProduct;

    }
</script>

<div class="container max-w-lg  my-4 mx-auto p-5 ">
    <div>
        <h1 class="3-m font-bold text-slate-700 mb-1 text-center">Shop Now</h1>
    </div>
</div>


<div class="container mt-6 grid grid-cols-1 md:grid-cols-3 mx-auto gap-5 ">
    {#each products as product }
    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0 shadow-md">
        <div style="background-image: url({product.image});" class="image w-20"></div>
        <div class="">
            <p class="font-bold text-slate-700 text-md"> {product.name}</p>
            <p class="font-light text-slate-400">{product.harga}</p>

            <div>
                <p></p>

             <button type="button" on:click={() => addProduct(product)} class="mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> add to cart </button>

            <button type="button"  class=" md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
           
            <button type="button"  class="md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>

            
            <p class="flex"></p>


            </div>
            
        
        </div>
    </div>
    {/each}
    {#each products as product }
    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0 shadow-md">
        <div style="background-image: url({product.image});" class="image w-20"></div>
        <div class="">
            <p class="font-bold text-slate-700 text-md"> {product.name}</p>
            <p class="font-light text-slate-400">{product.harga}</p>
            
            <div>
                <p></p>

             <button type="button" on:click={() => addProduct(product)} class="mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> add to cart </button>

            <button type="button"  class=" md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
           
            <button type="button"  class="md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>

            
            <p class="flex"></p>


            </div>
            
        
        </div>
    </div>
    {/each}
    {#each products as product }
    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0 shadow-md">
        <div style="background-image: url({product.image});" class="image w-20"></div>
        <div class="">
            <p class="font-bold text-slate-700 text-md"> {product.name}</p>
            <p class="font-light text-slate-400">{product.harga}</p>
            
            <div>
                <p></p>

            <button type="button" on:click={() => addProduct(product)} class="mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> add to cart </button>

            <button type="button"  class=" md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
           
            <button type="button"  class="md:hidden mt-3 bg-lime-400 text-neutral-800 font-bold border-gray-300 focus:outline-none hover:bg-lime-500 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>

            
            <p class="flex"></p>


            </div>
            
        
        </div>
    </div>
    {/each}
</div>




<!-- Sudah berfungsi-->
<div class="container max-w-lg bg-white my-6 border-b-2 rounded-xl mx-auto p-5 shadow-sm">
    <div>
        <h1 class="3-m font-bold text-slate-700 mb-3">There are {cart.length} item in your cart</h1>
        <p class="text-slate-500">Pincode: 800015</p>
    </div>
</div>


<div class="container mt-3 grid grid-cols-1 md:grid-cols-3 mx-auto gap-5 ">
     {#each products as product }
    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0 shadow-md">
       
        <div class="image w-20" style="background-image: url({product.image});" >
            <div class="deskripsi">
                <h4>{product.name}</h4>
                <p>Rp {product.harga}</p>
                <button class="btn-cart" on:click={() => addToCart(product)}>Add to Cart</button>
            </div>
        </div> 

    
    </div>
     {/each} 
    <div class="card-list">
        {#each cart as item}
        {#if item.jumlah > 0}
        <div class="cart-item">
            <img width="50" src="{item.image}" alt="{item.name}">
            <p>{item.jumlah}</p>
            <button on:click={() => minusItem(item)}>-</button>
            <button on:click={() => plusItem(item)}>+</button>
            <button on:click={() => plusItem(item)}>x</button>
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
    
 
    .btn-cart{
        height: 50px;
        width: 100px;
        margin-bottom: -8px !important;
        border-radius: 20px;
        background-color: #e7c6a8;
        border: 0;
        font-size: 12px;
    }
    .btn-cart:hover{
        background-color: antiquewhite;
        cursor: pointer;
    }
    
    .total {
        margin-top: 125px;
        text-align: right;
    }
    
   
    .card-list {
        display: grid;
        grid-template-columns: repeat(3, 1fr );
    }
    .cart-item{
        margin-top: 210px;
    }
</style>

