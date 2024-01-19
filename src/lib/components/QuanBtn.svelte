<script>
  let quantity = 1;
  $: {
    if (quantity <= -1) {
      quantity = 0;
    }
  }
  console.log("quantity", quantity);
</script>

<div
  class="bg-blue-600 p-3 flex flex-row justify-between items-center w-2/5 text-lg text-black-500"
>
  <button
    class=" text-2xl hover:bg-gray-500 p-2 rounded hover:text-white"
    on:click={() => {
      quantity--;
    }}>-</button
  >
  <span>{quantity}</span>
  <button
    class=" text-2xl hover:bg-gray-500 p-2 rounded hover:text-white"
    on:click={() => {
      quantity++;
    }}>+</button
  >
</div>

<style>
</style>
