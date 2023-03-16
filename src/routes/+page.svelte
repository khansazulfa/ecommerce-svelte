<script>
	import { todos } from "../stores/formStore";
    import TodoForm from "../components/TodoForm.svelte";
    import Todo from "../components/Todo.svelte";
</script>

<div class="mt-6 ">
</div>

<main>

    <TodoForm/>

{#each $todos as todo}
    <Todo todo={todo} index={todo.id}/>
 {/each}
</main>