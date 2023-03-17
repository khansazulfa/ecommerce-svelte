<script>
import {addTodo} from "../stores/formStore";

  let todo = '';
    const handleSubmit = () => {
    addTodo(todo);
    todo = '';
    console.log("submitting")
  }
</script>

  
 


<form action="" class="my-6" on:submit|preventDefault={handleSubmit}> 
    <div class="flex flex-col text-sm mb-2 ml-5 mr-5">
        <label class="font-bold mb-2 text-gray-800 my-3" for="name">Todo</label>
        <input type="text" name="nama" placeholder="tulis disini" class=" px-5 py-2 border">
    </div> 
        <button type="submit" class="text-white shadow-lg px-5 py-2 my-2 shadow-cyan-500/50 ml-5 bg-sky-700 rounded ">Submit</button>
</form>