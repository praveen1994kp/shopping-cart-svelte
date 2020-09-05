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
        padding: .8rem;
        margin: .3rem;
        border-radius: .2rem;
        cursor: pointer;
    }
    div {
        flex-grow: 1;
        width: 50%;
        margin: 1rem;
    }
</style>