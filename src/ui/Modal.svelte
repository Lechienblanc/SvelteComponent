<script>
import Popup from "./Popup.svelte";
	
  export let showModal = false;
</script>

<svelte:head>
  {#if showModal}
    <style>
			:root {
				--filter: blur(2px);
			}
			
			@supports (backdrop-filter: var(--filter)) {
				#portals .backdrop {
					backdrop-filter: var(--filter);
				}
			}
			
			@supports not (backdrop-filter: var(--filter)) {
				.modal-active .app {
					filter: var(--filter);
				}
			}
    </style>
  {/if}
</svelte:head>

{#if showModal}
	<Popup target="#portals" bodyClass="modal-active">
		<div class="backdrop">
			<div class="dialog">
				<slot name="header" />
				<section class="content">
					<slot name="content" />
				</section>
				<slot name="footer" />
			</div>
		</div>
	</Popup>
{/if}

<style>
  .backdrop {
		position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 9999;
    box-shadow: inset 0px 0px 24rem rgba(0, 0, 0, 0.25);
    background-color: rgba(0, 0, 0, 0.25);
  }

  .dialog {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 48rem;
		max-width: 90%;
    max-height: 90vh;
    box-shadow: 0px 0px 2.4rem rgba(0, 0, 0, 0.1);
    transform: translate3d(-50%, -50%, 0);
    background-color: #FFF;
    margin: 0 auto;
    overflow: auto;
    color: black;
    border-radius: 10px;
    padding: 20px;
  }

  .content {
    position: relative;
  }
</style>