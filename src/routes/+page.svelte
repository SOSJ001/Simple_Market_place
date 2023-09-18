<script>
    import Button from "../lib/components/button.svelte";
    import Categories from "../lib/components/categories.svelte";
    import Different from "../lib/components/different.svelte";
    import Explain from "../lib/components/explain.svelte";
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
            class="p-10 md:flex md:flex-row grid grid-cols-2 items-center gap-5 justify-center"
        >
            <Product />
            <Product />
            <Product />
            <Product />
            <Product />
        </div>
        <Button />
    </div>
    <Explain />
</div>
