<script>
	let cart = [];
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
            return;
        }
    }
	 cart = [...cart, product]
 }
</script>

<p>There are {cart.length} item in your cart</p>

<div class="product-list">
    {#each products as product }
        <div 
            class="image" 
            style="background-image: url({product.image});">
        </div>

    <h4>{product.name}</h4>
        <p>Rp {product.harga}</p>
		<button on:click={() => addToCart(product)}>Add to Cart</button>
    {/each}
</div>
{JSON.stringify(cart)}

<style>
    .product-list {
        display: grid;
        grid-template-columns: auto auto;
        
    }
    .image{
        height: 150px;
        width:150px;
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
    }
</style>
   