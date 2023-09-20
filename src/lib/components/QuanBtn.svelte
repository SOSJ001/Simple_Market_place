<script>
    let quantity = 1;
    $: {
        if (quantity <= -1) {
            quantity = 0;
        }
        
    }
    console.log("quantity", quantity);
</script>

<div class="bg-blue-600 p-3 flex flex-row justify-between w-2/5 text-lg text-black-500">
    <a
        href=""
        class=" text-2xl"
        on:click={() => {
            quantity--;
        }}>-</a
    >
    <span>{quantity}</span>
    <a
        href=""
        class=" text-2xl"
        on:click={() => {
            quantity++;
        }}>+</a
    >
</div>
