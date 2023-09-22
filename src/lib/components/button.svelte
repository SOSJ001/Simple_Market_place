<script>
import { goto } from '$app/navigation';
  export let link = "/browsing";
  export let width = "w-auto";
  export let round = "rounded-lg";
  export let modal = "false";
  export let modalOpen= false;


  let navigate = (modal, link) => {
    if (modal === "true") {
      modalOpen = !modalOpen;
      console.log("modal is TRUE", modalOpen);
      return
    } else {
      goto(link);
      console.log("modal is FALSE", modal);

    }
  };
</script>

<div class="flex w-full justify-center items-center">
  <a href={link} class={width} on:click|preventDefault={navigate(modal,link)} >
    <button
      class="bg-blue-600 p-3 mb-3 {round} font-semibold hover:bg-blue-700 w-full"
    >
      <slot name="text">VIEW COLLECTION</slot>
    </button>
  </a>
</div>
