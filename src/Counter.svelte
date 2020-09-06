<script>
    export let count = 0;
    function handleIncrementClick() {
        count += 1;
    }
    function handleDecrementClick() {
        if(count > 0) {
            count -=1;
        }
    }
</script>
<div>
    <button on:click={handleDecrementClick}>-</button>
    <span>{count}</span>
    <button on:click={handleIncrementClick}>+</button>
</div>

<style>
    button {
        padding: .5rem;
        margin: .1rem;
        border-radius: .4rem;
        cursor: pointer;
    }
</style>