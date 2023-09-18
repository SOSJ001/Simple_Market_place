<script>
    import Categories from "../lib/components/categories.svelte";
    import Different from "../lib/components/different.svelte";
    import Hero from "../lib/components/hero.svelte";
    import Product from "../lib/components/product.svelte";
    import Top from "../lib/components/top.svelte";
</script>

<div class="bg-black-500 h-screen w-screen overflow-x-hidden">
    <Top />
    <Categories />
    <Hero />
    <Different />
    <div class=" bg-gray-500 flex flex-col items-center justify-center">
        <div
            class="p-10  md:flex md:flex-row grid grid-cols-2 items-center gap-3 justify-center"
        >
            <Product />
            <Product />
            <Product />
            <Product />
            <Product />
        </div>
        <div>
            <button
                class="bg-blue-600 p-3 rounded-lg font-semibold hover:bg-blue-700"
            >
                VIEW COLLECTION
            </button>
        </div>
    </div>
</div>
