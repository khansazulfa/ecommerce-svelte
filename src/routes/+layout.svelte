<script>
    import "../app.css";
    import { cartProduct } from '../stores/formStore';
    import { pageSelected } from '../stores/formStore';

    let cart = [];
    let products = [];

    const addToCart= (products) => {
        alert (JSON.stringify(products))
    }  
</script>

<!--Navbar-->
<div>
    <nav class="bg-white dark:bg-gray-800  shadow ">
        <div class="px-8 mx-auto max-w-7xl">
            <div class="flex items-center justify-between h-16">
                <div class=" flex items-center">
                    <a class="flex-shrink-0" href="/">
                        <span class="ml-auto text-2xl font-bold text-lime-600 tracking-wide mr-6">Tokoku</span>
                    </a>
                    <div class="hidden md:block">
                        <div class="flex items-baseline ml-6 space-x-4">
                            <a class="hover:text-lime-600 dark:hover:text-white px-3 py-2 rounded-md text-md font-bold" href="/">
                                Home
                            </a>
                            <a class="hover:text-lime-600 dark:hover:text-white px-3 py-2 rounded-md text-md font-bold" href="/product">
                                Product
                            </a>
                            <a class="hover:text-lime-600 dark:hover:text-white px-3 py-2 rounded-md text-md font-bold" href="/cart">
                                Cart
                            </a>
                            <a class="hover:text-lime-600 dark:hover:text-white px-3 py-2 rounded-md text-md font-bold" href="/order">
                                Order
                            </a>
                        </div>
                    </div>
                </div>
                <div class="block">
                    <div class="flex items-center ml-4 md:ml-6">
                        <div class="relative ml-3">
                            <div class="relative inline-block text-left">
                                <div class="flex">
                                    <button on:click={() => addToCart(products)} type="button" class="  flex items-center justify-center w-full rounded-md  px-4 py-2 text-sm font-medium hover:text-lime-600" id="options-menu"> 
                                        <i class="fa fa-shopping-cart"></i>
                                        <span class="absolute insert-0 object-right-top -mr-6">
                                            <div class="inline-flex items-center px-1.5 py-0.5 bg-red-600 text-white
                                            rounded-full ml-2">
                                            {$cartProduct.length}
                                        </div>
                                    </span>
                                </button>
                                <button type="button" class=" items-center justify-center w-full rounded-md -mt-1 px-4 py-2 text-sm font-medium hover:text-lime-600" id="options-menu"> 
                                    <a href="/signIn">
                                    <i class="fa fa-user w-6"></i></a>
                                    <span class="absolute insert-0 object-right-top -mr-6">
                                    </span>
                                 </button>
                            </div>

                        </div>
                    </div>
                </div>
            </div>
            <div class="flex -mr-2 md:hidden">
                <button class="text-gray-800 dark:text-white hover:text-gray-300 inline-flex items-center justify-center p-2 rounded-md focus:outline-none">
                    <svg width="20" height="20" fill="currentColor" class="w-8 h-8" viewBox="0 0 1792 1792" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1664 1344v128q0 26-19 45t-45 19h-1408q-26 0-45-19t-19-45v-128q0-26 19-45t45-19h1408q26 0 45 19t19 45zm0-512v128q0 26-19 45t-45 19h-1408q-26 0-45-19t-19-45v-128q0-26 19-45t45-19h1408q26 0 45 19t19 45zm0-512v128q0 26-19 45t-45 19h-1408q-26 0-45-19t-19-45v-128q0-26 19-45t45-19h1408q26 0 45 19t19 45z">
                        </path>
                    </svg>
                </button>
            </div>
        </div>
    </div>
    <div class="md:hidden">
        <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
            <a class=" hover:text-lime-600 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/">
                Home
            </a>
            <a class="hover:text-lime-600 dark:text-white block px-3 py-2 rounded-md text-base font-medium" href="/product">
                Product
            </a>
            <a class=" hover:text-lime-600 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/cart">
                Cart
            </a>
            <a class=" hover:text-lime-600 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/order">
                Order
            </a>
        </div>
    </div>
</nav>
</div>


<div class="container">
    <slot />
</div>


<!--Footer-->
<div class="footer py-12 bg-lime-900 text-white" id="footer">
    <div class="container mx-auto px-4">
        <div class="footer-box flex justify-around lg:flex-row flex-col lg:gap-0 gap-10">
            <div class="box lg:w-[500px]">
                <div class="logo flex items-center gap-2">
                    <img src="/src/images/logo.png" alt="logo" class="w-16 rounded-full">
                    <h1 class="font-bold text-2xl">Truly</h1>
                </div>
                <div class="desc">
                    <p class="opacity-50 text-base leading-loose">Truly a platform concentrating on healthy lifestyle and healthy food.</p>
                </div>
            </div>
            <div class="box lg:w-[100px] gap-2 flex flex-col">
                <h4 class="font-blod text-lg">Menu</h4>
                <a href="/" class="opacity-50 hover:opacity-100">Home</a>
                <a href="/about" class="opacity-50 hover:opacity-100">About</a>
                <a href="/product" class="opacity-50 hover:opacity-100">Product</a>
                <a href="/project" class="opacity-50 hover:opacity-100">Project</a>
                <a href="/contact" class="opacity-50 hover:opacity-100">Contact</a>
            </div>
            <div class="box lg:w-[200px] gap-2 flex flex-col">
                <h4 class="font-blod text-lg">Company</h4>
                <a href="#x" class="opacity-50 hover:opacity-100">Terms of Services</a>
                <a href="#x" class="opacity-50 hover:opacity-100">Privacy Policy</a>
                <a href="#x" class="opacity-50 hover:opacity-100">Blog</a>
                <a href="#x" class="opacity-50 hover:opacity-100">Cookies Setting</a>
            </div>
        </div>
    </div>
</div>
<!--Tutup Footer-->

<!--Button back to top-->
<a href="#home">
    <i class="fa-solid fa-circle-arrow-up fixed bottom-10 right-10 text-5xl text-lime-600 cursor-pointer hover:text-lime-700 z-20 " title="Kembali ke Atas"></i>
</a>
<style>
    
    nav{
        padding: 0.5em;
    } 
    
    
</style>

