<script>
import { goto } from '$app/navigation';
  export let link = "/browsing";
  export let width = "w-auto";
  export let round = "rounded-lg";
  export let modal = false;

//   let navigate = (modal, link) => {
//     if (!modal) {
//       modal = !modal;
//       console.log("modal", modal);
//       return
//     } else {
//       goto(link);
//       console.log("modal", modal);
    //   on:click|preventDefault={navigate(link, modal)

//     }
//   };
</script>

<div class="flex w-full justify-center items-center">
  <a href={link} class={width} >
    <button
      class="bg-blue-600 p-3 mb-3 {round} font-semibold hover:bg-blue-700 w-full"
    >
      <slot name="text">VIEW COLLECTION</slot>
    </button>
  </a>
</div>
