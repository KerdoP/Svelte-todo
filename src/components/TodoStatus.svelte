<script>
    export let todos;
    export function focus() {
        // shorter version: export const focus = () => headingEl.focus()
        headingEl.focus();
    }
    $: totalTodos = todos.length;
    $: completedTodos = todos.filter((todo) => todo.completed).length;

    let headingEl;
</script>

<h2 id="list-heading" bind:this={headingEl} tabindex="-1">
    {completedTodos} out of {totalTodos} items completed
</h2>
