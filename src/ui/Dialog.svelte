<script>
    import Modal from "./Modal.svelte";

    let showModal = false;
    const toggleModal = () => (showModal = !showModal);
</script>

<div class="app">
    
    <button class="btnMod" on:click={toggleModal}>Show Modal</button>

    <Modal bind:showModal>
        <header slot="header" class="headModal">
            <h1 class="modal-title">Information</h1>
        </header>
        <section class="modal-content" slot="content">
            <div class="flex1">
                <label class="name"> Name </label>
                <input id="Name" placeholder="John Doe" />
            </div>
            <div class="flex1">
                <label class="pwd"> Password</label>
                <input id="pwd" placeholder="password" />
            </div>
        </section>
        <footer class="modal-actions" slot="footer">
            <button class="btnDial" on:click={toggleModal}>Save Changes</button>
        </footer>
    </Modal>
</div>

<div id="portals">
    <!-- modals will be appended here -->
</div>

<style>
    :global(html) {
        font-size: 62.5%;
    }

    :global(body) {
        font-size: 1.6rem;
        box-sizing: border-box;
    }

    .headModal {
        margin-bottom: 21px;
    }

    .modal-title {
        padding: 0;
        margin: 0;
    }

    .modal-content {
        display: flex;
        flex-direction: column;
        gap: 21px;
        padding: 0;
    }

    .flex1 {
        display: flex;
        flex-direction: column;
    }
    .modal-actions {
        padding: 1.8rem 0 1.8rem;
        text-align: right;
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

    .btnDial {
        border-radius: 10px;
    }

    btnMod:hover,
    btnDial {
        opacity: 0.8;
    }
</style>
