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
        <li><h4>Item</h4><h4>Count</h4></li>
        {#each items as item (item.id)}
            <li>
                <span>{item.name}: </span>
                <Counter bind:count={item.count} />
            </li>
        {/each}
    </ul>
</div>

<style>
    .container {
        margin: 0 auto;
        min-width: 15em;
        width: 60%;
        line-height: 1.1;
    }

    ul {
        list-style-type: none;
        padding: 0 .3em;
        margin: 0;
    }

    li {
        display: grid;
        grid-template-columns: 1fr 1fr;
        justify-items: center;
        align-items: center;
        border-bottom: .1em solid #cacaca;
        padding: .8em 0;
    }
    h4 {
        text-align: center;
        width: 100%;
    }
    span {
        width: 100%;
        text-align: right;
        font-size: .95em;
    }
</style>