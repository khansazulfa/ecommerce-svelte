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

<div class="shipping-order">
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
</div>

<style>
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
</style>