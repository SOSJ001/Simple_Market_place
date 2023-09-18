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
    <div class="p-10 bg-gray-500 md:flex md:flex-row grid grid-cols-2 items-center gap-5 justify-center">
       <Product/>
       <Product/>
       <Product/>
       <Product/>
    </div>
</div>
