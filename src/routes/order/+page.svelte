<script>
let address = {
    name:"",
    email:"",
    phone:"",
    street:"",
}

</script>

<div class="shipping-order">
    <div>
        <p>Name</p>
        <input bind:value={address.name}/>
        <p>Email</p>
        <input bind:value={address.email} />
        <p>Phone</p>
        <input bind:value={address.phone} />
        <p>Address</p>
        <textarea bind:value={address.street} col="24" rows="6"></textarea>
        <br>
        <button class="btn">Checkout</button>
    </div>
    <div class="current-address">
        <p>{address.name}</p>
        <p>{address.email}</p>
        <p>{address.phone}</p>
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