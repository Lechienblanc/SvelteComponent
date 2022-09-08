<script>
    let items = ['Hetic','EEMI', 'Epitech', 'Etna']



 
</script>

<main>
    
    <select class="btnMod" value={items} >
        {#each items as item}
            <option value={item}>
                {item}
            </option>
        {/each}
    </select>
</main>

<style>
    .btnMod {
        border: 1px solid #333;
        border-radius: 0;
        background: none;
        padding: 0.8rem 1.6rem;
        min-width: 9.6rem;
        border-radius: 10px;
    }
</style>