<script>
    import Counter from "./Counter.svelte";
    let items = [
        {id: 1, name: "Wireless Keyboard", count: 0, price: 670},
        {id: 2, name: "LG 4k Curved Monitor", count: 0, price: 39000},
        {id: 3, name: "Nvidia RTX 3078", count: 0, price: 32000},
        {id: 4, name: "256GB nVme SSD", count: 0, price: 4000}
    ]

</script>

<div class="container">
    <ul>
        <li><h4>Item</h4><h4>Count</h4><h4>Price</h4></li>
        {#each items as item (item.id)}
            <li>
                <span>{item.name}: </span>
                <Counter bind:count={item.count} />
                <span>&#8360;. {item.price.toFixed(2)}</span>
            </li>
        {/each}
    </ul>
</div>

<style>
    .container {
        max-width: 1200px;
        width: 80%;
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow: 3px 0px 17px #888888;
        margin: auto
    }
    ul {
        list-style: none;
        width: 100%;
    }
    li {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    li > * {
        width: 50%;
        flex-grow: 1;
        margin: 1rem;
    }
</style>