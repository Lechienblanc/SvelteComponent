<script>
    let visible = false;

    const pop = () => {
        visible = true;
    };
</script>


<button class='btnMod'on:click={pop}> Typo </button>

{#if visible}
    <div
        role="dialog"
        aria-labelledby="Title"
        aria-describedby="Description"
        aria-orientation="vertical"
        class="popover"
        on:click|stopPropagation
    >
        <div
            on:click|stopPropagation={() => (visible = false)}
            class="backdrop"
        />
        <div class="wrapper">
            <div align="left" >Description</div>

            <div class="flex1">
                <label class="size"> Name </label>
                <input id="size" value="15px" />
            </div>

            <div class="flex1">
                <label class="height"> Height </label>
                <input id="size" value="15px" />
            </div>

        </div>
    </div>
{/if}

<style>
    .backdrop {
        position: absolute;
        inset: 0;
        background: rgba(0, 0, 0, 0.3);
    }

    .wrapper {
        position: absolute;
        min-width: 200px;
        max-width: 200px;
        min-height: 100px;
        width: fit-content;
        height: fit-content;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        background: white;
        color: black;
        border-radius: 6px;
        padding: 20px;
        justify-content: space-between;
    }

    .flex1 {
        all: unset;
        display: flex;
        gap: 20px;
    }

    .btnMod {
        cursor: pointer;
        border: 1px solid #333;
        border-radius: 0;
        background: none;
        padding: 0.8rem 1.6rem;
        min-width: 9.6rem;
        border-radius: 10px;
    }
    .size{
        margin-right: 15px;
    }

    #size {
        all: unset;
        width: 100%;
        box-shadow: #1a1a1a 0px 0px 0px 1px;
        border-radius: 6px;
        display: flex;
        justify-content: center;
        align-content: center;
    }
</style>
