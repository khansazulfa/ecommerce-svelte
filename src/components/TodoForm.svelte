<script>
import {addTodo} from "../stores/formStore";

  let todo = '';
    const handleSubmit = () => {
    addTodo(todo);
    todo = '';
    console.log("submitting")
  }
</script>

    <!--Header-->
<div class="header min-h-screen flex items-center">
    <div class="container mx-auto px-4 ">
        <div class="header-box flex lg:flex-row flex-col items-center gap-10" >
            <div class="box lg:w-1/2 lg:order-1 order-2 text-center lg:text-left">
                <h1 class="font-extrabold md:text-4xl sm:text-3xl text-2xl mb-4 text-slate-900 animate__animated animate__fadeInUp animate__delay-1s">Truly a platform concentrating on healthy lifestyle and healthy food.</h1>
                <p class="mb-4 text-slate-400 md:text-base sm:text-sm text-xs animate__animated animate__fadeInUp animate__delay-1s">Truly is a platform that provides information about a healthy lifestyle, exercise, healthy organic food, managing calories, and much more</p>
                <button class="w-48 h-12 bg-lime-600 rounded-lg font-bold hover:bg-lime-700 cursor-pointer text-white animate__animated animate__fadeInUp animate__delay-1s">About Truly</button>
            </div>
            <div class="box lg:w-1/2 lg:order-2 order-1 lg:pt-0 pt-10">
                <img src="/src/images/slogan.jpg" alt="header" class="xl:w-[500px] lg:w-[400px] md:w-[300px] sm:w-[250px] w-[200px] block ml-auto animate__animated animate__fadeInUp animate__delay-1s">
            </div>
        </div>
    </div>
</div>
    <!--Tutup Header-->

<form action="" class="my-6" on:submit|preventDefault={handleSubmit}> 
    <div class="flex flex-col text-sm mb-2 ml-5 mr-5">
        <label class="font-bold mb-2 text-gray-800 my-3" for="name">Todo</label>
        <input type="text" name="nama" placeholder="tulis disini" class=" px-5 py-2 border">
    </div> 
        <button type="submit" class="text-white shadow-lg px-5 py-2 my-2 shadow-cyan-500/50 ml-5 bg-sky-700 rounded ">Submit</button>
</form>