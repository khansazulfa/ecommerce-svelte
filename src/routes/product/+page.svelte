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

<div class="container max-w-lg bg-white my-6 border-b-2 rounded-xl mx-auto p-5 shadow-sm">
    <div>
        <h1 class="3-m font-bold text-slate-700 mb-3">My Cart</h1>
        <p class="text-slate-500">Pincode: 800015</p>
    </div>
</div>


<div class="container shadow-sm mt-6 grid grid-cols-1 md:grid-cols-4 mx-auto gap-5">
    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0">
        <div > 
            <img src="src/images/apple.png" alt="apple" class="w-20">
        </div>
        <div class="ml-4">
            <p class="font-bold text-slate-700 text-md"> Apple</p>
            <p class="font-light text-slate-400">Rp 10.000 / kg</p>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>
           
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
        </div>
    </div>

     <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0">
        <div > 
            <img src="src/images/orange.png" alt="orange" class="w-20">
        </div>
        <div class="ml-4">
            <p class="font-bold text-slate-700 text-md">Orange</p>
            <p class="font-light text-slate-400">Rp 8.000 / kg</p>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>
           
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300  focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
        </div>
    </div>

     <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0">
        <div > 
            <img src="src/images/strawberry.png" alt="strawberry" class="w-20">
        </div>
        <div class="ml-4">
            <p class="font-bold text-slate-700 text-md">Strawberry</p>
            <p class="font-light text-slate-400">Rp 20.000 / kg</p>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300  focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
        </div>
    </div>

    <div class="relative bg-gray-100 rounded-md p-5 flex mx-5 md:mx-0">
        <div > 
            <img src="src/images/strawberry.png" alt="strawberry" class="w-20">
        </div>
        <div class="ml-4">
            <p class="font-bold text-slate-700 text-md">Strawberry</p>
            <p class="font-light text-slate-400">Rp 20.000 / kg</p>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300  focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> - </button>
            <button type="button" class="mt-3 bg-orange-200 text-orange-500 font-bold border-gray-300 focus:outline-none hover:bg-orange-300 focus:ring-4 focus:ring-gray-200 rounded-full text-sm px-4 py-1  mr-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark-focus:ring-gray-700"> + </button>
        </div>
    </div>

    
</div>
