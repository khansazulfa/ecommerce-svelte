<script>
    import { todos } from "../stores/formStore";
    import TodoForm from "../components/TodoForm.svelte";
    import Todo from "../components/Todo.svelte";
    import '../app.css';
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

<!--About--> 
<div class="about py-16">
    <div class="container mx-auto px-4">
        <div class="about-box">
            <div class="box text-center">
                <h1 class="font-extrabold text-4xl mb-8 text-slate-900 "  >About Us</h1>
                <p class="lg:w-3/4 w-full mx-auto md:text-base text-xs text-slate-400" >Truly is a platform that provides information about a healthy lifestyle. Really will contribute to friends who want a healthy lifestyle to maintain a healthy body in terms of exercise, what food we consume, how many calories we need and we sell healthy organic food, and journals about a healthy lifestyle. Full of love from us <i class="fa-solid fa-heart text-lime-500"></i></p>
            </div>
            <div class="box pt-16">
                <img src="/src/images/about1.svg" alt="undraw.co" class="md:w-[400px] w-[200px] mx-auto">
            </div>
        </div>
    </div>
</div>
<!--Tutup about-->

<!--Product-->
<div class="product py-32" id="product">
    <div class="container mx-auto px-4">
        <div class="product-box ">
            <div class="box text-center">
                <h1 class="font-extrabold text-4xl mb-6 text-slate-900" >Product</h1>
                <p class="md:w-3/4 w-full mx-auto md:text-base sm:text-sm text-xs text-slate-400" >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facere ipsam distinctio quibusdam cumque repellendus accusantium beatae, labore tempora sit fuga earum in iure vitae aut animi nihil quaerat odio veniam.</p>
            </div>
            <div class="box grid md:grid-cols-2 grid-cols-1 gap-16 pt-16 items-center">
                <img src="assets/image/Services.svg" alt="" class="w-[450px] md:justify-self-end justify-self-center" >
                <div class="desc md:justify-self-start justify-self-center" >
                    <p class="flex items-center gap-4 text-xl font-bold mb-6">
                        <i class="fa-solid fa-circle-check text-4xl text-lime-600"></i> Langkah awal menuju sukses</p>
                    <p class="flex items-center gap-4 text-xl font-bold mb-6">
                        <i class="fa-solid fa-circle-check text-4xl text-lime-600"></i> Impianmu sebentar lagi tercapai</p>
                    <p class="flex items-center gap-4 text-xl font-bold mb-6">
                        <i class="fa-solid fa-circle-check text-4xl text-lime-600"></i> Kesempatan kamu hanya hari ini</p>
                    <p class="flex items-center gap-4 text-xl font-bold mb-6">
                        <i class="fa-solid fa-circle-check text-4xl text-lime-600"></i> Gabung dengan kami sekarang juga, apa yang kamu tunggu?</p>
                </div>
            </div>
        </div>
    </div>
</div>
<!--Tutup Product-->

<!--Project-->
    <div class="project py-32" id="project">
        <div class="container mx-auto px-4">
            <div class="project-box">
                <div class="box text-center">
                    <h1 class="font-extrabold text-4xl mb-6 text-slate-900">Project</h1>
                    <p class="text-slate-400">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Mollitia laudantium eius illum asperiores! Aspernatur odio hic rerum aliquam ipsa, sunt omnis ratione temporibus eveniet porro sed labore quam, repellendus perferendis.</p>
                </div>
                <div class="box flex items-center justify-center gap-4 flex-wrap pt-12">
                    <div class="p-16 text-center bg-lime-100" >
                    <h1 class=" text-4xl font-bold mb-2">2000</h1>
                    <p>Orang Bergabung</p>
                    </div>
                    <div class="p-16 text-center bg-lime-500" >
                    <h1 class=" text-4xl font-bold mb-2">2000</h1>
                    <p>Orang Bergabung</p>
                    </div>
                    <div class="p-16 text-center bg-lime-100" >
                    <h1 class=" text-4xl font-bold mb-2">2000</h1>
                    <p>Orang Bergabung</p>
                    </div>
                </div>
                <div class="box flex justify-center items-center flex-wrap gap-4 pt-16">
                <img src="assets/image/services1.jpg" alt="unsplas.com" class="w-[300px] h-[250px]"/>
                <img src="assets/image/services2.jpg" alt="unsplas.com" class="w-[300px] h-[250px]" />
                <img src="assets/image/services3.jpg" alt="unsplas.com" class="w-[300px] h-[250px]"/>
                <img src="assets/image/services4.jpg" alt="unsplas.com" class="w-[300px] h-[250px]"/>
                <img src="assets/image/services5.jpg" alt="unsplas.com" class="w-[300px] h-[250px]"/>
                <img src="assets/image/services6.jpg" alt="unsplas.com" class="w-[300px] h-[250px]"/>
                </div>
            </div>
        </div>
    </div>
<!--Tutup Project-->

<!--Contact-->
<div class="contact py-32" id="contact">
    <div class="container mx-auto px-4">
        <div class="contact-box">
            <div class="box text-center">
                <h1 class="font-extrabold text-4xl mb-6 text-slate-900" >Contact</h1>
                <p class="text-slate-400" >Lorem ipsum dolor sit amet, consectetur adipisicing elit. </p>
            </div>
           <form action="https://formsubmit.co/khansasz95@gmail.com" method="POST" class="mt-10 ">
            <table class="mx-auto lg:w-3/5 w-3/4">
                <tr>
                    <td><input type="text" name="Nama Lengkap" placeholder="Nama Lengkap.." autocomplete="off" required class="w-full h-12 rounded-md border p-3"/></td>
                </tr>
                 <tr>
                    <td><input type="email" name="email" placeholder="Your Email.." autocomplete="off" required class="w-full h-12 rounded-md border p-3"/></td>
                </tr>
                 <tr>
                    <td><textarea name="Pesan" id="" cols="30" rows="10" placeholder="Pesan" autocomplete="off" required class="w-full rounded-md border p-3"></textarea></td>
                </tr>
                <tr>
                    <td><button type="submit"class="w-40 h-10 bg-lime-600 ml-auto block cursor-pointer font-bold rounded hover:bg-lime-700 text-white">Kirim!</button></td>
                </tr>
            </table>
           </form>
        </div>
    </div>
</div>
<!--Tutup Contact-->


<TodoForm/>

{#each $todos as todo}
<Todo todo={todo} index={todo.id}/>
{/each}
