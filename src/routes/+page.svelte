<script>
    import Categories from "../lib/components/categories.svelte";
    import Different from "../lib/components/different.svelte";
    import Hero from "../lib/components/hero.svelte";
    import Listings from "../lib/components/listings.svelte";
    import Top from "../lib/components/top.svelte";
</script>

<div class="bg-black-500 h-screen w-screen overflow-x-hidden">
    <Top />
    <Categories />
    <Hero />
    <Different />
    <Listings/>
</div>
