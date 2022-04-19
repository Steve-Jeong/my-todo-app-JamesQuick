<script>
  import TodoForm from '$lib/TodoForm.svelte'
  import Todo from '$lib/Todo.svelte'
  import {todos} from '../stores/todoStore.js'
</script>
<main>
  <h1 class="text-2xl font-bold text-center text-gray-700 md:text-4xl">My Todos</h1>
  <TodoForm />
  {#each $todos as todo}
    <Todo todo={todo} index={todo.id} />
  {/each}
</main>