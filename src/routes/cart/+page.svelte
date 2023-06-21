<script>
import { cartProduct } from './../../stores/formStore.js';
    
</script>

<div class="container max-w-lg bg-white my-6 border-b-2 rounded-xl mx-auto p-5 shadow-sm">
    <div>
        <h1 class="3-m font-bold text-slate-700 mb-3">My Cart</h1>
        <p class="text-slate-500">Pincode: 800015</p>
    </div>
</div>

<div class="mt-4 w-full">
    
     <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="nama-barang">Nama Barang</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"/>
    </div>
     <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="jumlah-pesana">Jumlah Pesanan</label>
        <input class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" />
    </div>
</div>

<style>
    h3{
        text-align: center;
    }
table, td, th {
    border: 1px solid #a5a5a5;
    height: 50px;
}

table {
    border-collapse: collapse;
    width: 100%;
}
</style>