<script> 
    
    let cart=[];
    let address = {
        name:"",
        email:"",
        phone:"",
        jumlah_pesanan:"",
        street:"",
    }
    
    const checkOut = () => {
        alert(JSON.stringify(cart)),
        alert(JSON.stringify(address))
    }
</script>

<div class="container max-w-lg bg-white my-6 border-b-2 rounded-xl mx-auto p-5 shadow-sm">
    <div>
        <h1 class="3-m font-bold text-slate-700 mb-3">Shipping order</h1>
        <p class="text-slate-500">Pincode: 800015</p>
    </div>    
</div>
<div class="mt-4 w-full">
    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="name">Name</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.name}/>
    </div>
    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="email">Email</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.email}/>
    </div>
    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="phone">Phone</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.phone}/>
    </div>
     <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="nama-barang">Nama Barang</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.phone}/>
    </div>
     <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="jumlah-pesana">Jumlah Pesanan</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.jumlah_pesanan}/>
    </div>
     <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="address">Alamat</label>
        <textarea class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" bind:value={address.street}/>
    </div>
</div>

<!-- <div class="shipping-order">
    <div>
        <h3>Shipping order</h3>
        <p>Name</p>
        <input bind:value={address.name}/>
        <p>Email</p>
        <input bind:value={address.email} />
        <p>Phone</p>
        <input bind:value={address.phone} />
        <p>Jumlah Pesanan</p>
        <input bind:value={address.jumlah_pesanan} />
        <p>Alamat</p>
        <textarea bind:value={address.street} col="24" rows="6"></textarea>
        <br>
        <button on:click={checkOut} class="btn" >Checkout</button>
    </div>
    <div class="current-address">
        <p>{address.name}</p>
        <p>{address.email}</p>
        <p>{address.phone}</p>
        <p>{address.jumlah_pesanan}</p>
        <p>{address.street}</p>
    </div>
</div> -->

<!-- <style>
    .shipping-order{
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 1em;
    }
    .current-address{
        padding: 2em;
        border: 2px dashed green;
    }
    .btn{
        margin-top: 8px;
        height: 35px;
        width: 185px;
        margin-bottom: -8px !important;
        border-radius: 10px;
        background-color: #f0cfb1;
        border: 0;
    }
    .btn:hover:hover{
        background-color: antiquewhite;
        cursor: pointer;
    }
</style> -->