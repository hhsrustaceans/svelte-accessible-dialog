<script>
  import { DialogOverlay, DialogContent } from "../../";
  import ScrollWrapper from "../helpers/ScrollWrapper.svelte";

  let isOpen = false;

  const closeDialog = () => {
    isOpen = false;
  };

  const openDialog = () => {
    isOpen = true;
  };
</script>

<ScrollWrapper>
  <button on:click={openDialog}>Open Dialog</button>

  <DialogOverlay {isOpen} onDismiss={closeDialog}>
    <DialogContent style="background: white; padding: 1rem; margin: 15vh auto; width: 50vw">
      <button on:click={closeDialog}>close modal</button>
      <h2>I am a dialog</h2>
    </DialogContent>
  </DialogOverlay>
</ScrollWrapper>
