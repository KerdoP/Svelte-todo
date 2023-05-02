<script>
    import { createEventDispatcher } from "svelte";

    export let todos;

    const dispatch = createEventDispatcher();
    const checkAll = () => {
        dispatch("checkAll", completed);
        completed = !completed;
    };
    const removeCompleted = () => dispatch("removeCompleted");

    let completed = true;

    $: completedTodos = todos.filter((t) => t.completed).length;
</script>

<div class="btn-group">
    <button
        type="button"
        class="btn btn__primary"
        disabled={todos.length === 0}
        on:click={checkAll}>{completed ? "Check" : "Uncheck"} all</button
    >
    <button
        type="button"
        class="btn btn__primary"
        disabled={completedTodos === 0}
        on:click={removeCompleted}>Remove completed</button
    >
</div>
