<script>
    import "../app.css";
    import { cartProduct } from '../stores/formStore';
    
</script>


<div>
    <nav class="bg-white dark:bg-gray-800  shadow ">
        <div class="px-8 mx-auto max-w-7xl">
            <div class="flex items-center justify-between h-16">
                <div class=" flex items-center">
                    <a class="flex-shrink-0" href="/">
                        <img class="w-8 h-8" src="https://www.tailwind-kit.com/icons/rocket.svg" alt="Workflow"/>
                    </a>
                    <div class="hidden md:block">
                        <div class="flex items-baseline ml-10 space-x-4">
                            <a class="text-gray-300  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium" href="/">
                                Home
                            </a>
                            <a class="text-gray-800 dark:text-white  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium" href="/product">
                                Product
                            </a>
                            <a class="text-gray-300  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium" href="/chart">
                                Cart
                            </a>
                            <a class="text-gray-300  hover:text-gray-800 dark:hover:text-white px-3 py-2 rounded-md text-sm font-medium" href="/order">
                                Order
                            </a>
                        </div>
                    </div>
                </div>
                <div class="block">
                    <div class="flex items-center ml-4 md:ml-6">
                        <div class="relative ml-3">
                            <div class="relative inline-block text-left">
                                <div>
                                    <button type="button" class="  flex items-center justify-center w-full rounded-md  px-4 py-2 text-sm font-medium text-gray-700 dark:text-gray-50 hover:bg-gray-50 dark:hover:bg-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-gray-500" id="options-menu">
                                     <i class="material-icons">shopping_cart</i>
                                        <span class="absolute insert-0 object-right-top -mr-6">
                                          <div class="inline-flex items-center px-1.5 py-0.5 bg-red-600 text-white
                                            rounded-full ml-2">
                                         {$cartProduct.length}
                                          </div>
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
                <a class="text-gray-300 hover:text-gray-800 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/">
                    Home
                </a>
                <a class="text-gray-800 dark:text-white block px-3 py-2 rounded-md text-base font-medium" href="/product">
                    Product
                </a>
                <a class="text-gray-300 hover:text-gray-800 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/chart">
                    Cart
                </a>
                <a class="text-gray-300 hover:text-gray-800 dark:hover:text-white block px-3 py-2 rounded-md text-base font-medium" href="/order">
                    Order
                </a>
            </div>
        </div>
    </nav>
</div>



<div class="container">
<slot />
</div>

<style>
nav{
  padding: 0.5em;
} 


</style>

