<script>
export let index;
export let todo;
export let editTodo;
export let removeTodo;
</script>
<div class = "todo">
    <p>
    {index+1}. {todo}
    </p>
    <div class = "actions">
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <i on:click={() => {
            editTodo(index)
        }} on:keydown={()=>{}} class="fa-regular fa-pen-to-square"></i>
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <i on:click={() => {
            removeTodo(index)
        }} on:keydown={()=>{}} class="fa-solid fa-trash-can"></i>                </div>
</div>
<style>
     .todo{
        border-left: 1px solid cyan;
        padding: 8px 14px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .actions{
        display: flex;
        gap: 8px;
        align-items: center;
        font-size: 1.3rem;
    }
    .actions i:hover{
        color: coral;
    }
    .actions i {
        cursor: pointer;
    }
</style>