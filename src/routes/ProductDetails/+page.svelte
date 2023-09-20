<script>
    import Top from "$lib/components/top.svelte";
    import AlsoLike from "../../lib/components/alsoLike.svelte";
    import Details from "../../lib/components/details.svelte";
    import Different from "$lib/components/different.svelte";
    import CallToAction from "$lib/components/callToAction.svelte";
    import Footer from "$lib/components/footer.svelte";
</script>

<div class="bg-black-500 h-screen w-screen overflow-x-hidden">
    <Top />
    <Details />
    <AlsoLike />
    <Different />
    <CallToAction />
    <Footer/>
</div>
