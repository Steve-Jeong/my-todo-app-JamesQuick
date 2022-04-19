<script>
  let todo = '';
  import {addTodo} from '../stores/todoStore'
  const handleSubmit = () => {
    addTodo(todo);
    todo = ''
    console.log('Submitting')
  }
</script>
<form 
  class='my-6' 
  action="/" 
  on:submit|preventDefault={handleSubmit}>
  <div 
    class='flex flex-col text-sm mb-2'>
    <label 
      class='font-bold mb-2 text-green-800' 
      for="todo">Todo
    </label>
    <input 
      class='appearance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg' 
      type='text' 
      name='todo' 
      placeholder="Watcha gotta do?" 
      bind:value={todo} 
    />
  </div>
  <button 
    class='w-full shadow-sm rounded bg-blue-500 hover:border-blue-100 text-white py-2 px-4'
    type='submit'>Submit
  </button>
</form>