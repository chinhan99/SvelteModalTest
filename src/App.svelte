<script>
  import { writable } from "svelte/store";
  import Modal, { bind } from "svelte-simple-modal";
  import Popup from "./Popup.svelte";
  import Counter from "./Counter.svelte";
  const modal = writable(null);
  const showModal = () => modal.set(bind(Popup, { message: "Surprise" }));
</script>

<Modal show={$modal}>
  <button on:click={showModal}>Show modal</button>
  <Counter />
</Modal>
