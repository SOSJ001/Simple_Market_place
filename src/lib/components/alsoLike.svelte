<script>
    import Button from "./button.svelte";
    import Product from "./product.svelte";
</script>

<div class="flex flex-col gap-10 bg-gray-500 py-10 px-5 md:m-10">
    <span class="text-2xl text-white font-medium"
        >You might also love these</span
    >
    <div class="w-full flex flex-col justify-center items-center gap-5">
        <div
            class="  md:flex md:flex-row grid grid-cols-2 items-center gap-5 justify-center"
        >
            <Product />
            <Product />
            <Product />
            <Product />
            <Product />
        </div>
        <Button>
            <span slot="text"> See Collection </span>
        </Button>
    </div>
</div>
