<script>
    import Filter from "../../lib/components/filter.svelte";
    import FilterBtn from "../../lib/components/filterBtn.svelte";
    import Top from "../../lib/components/top.svelte";
    import Product from "../../lib/components/product.svelte";
    import Button from "../../lib/components/button.svelte";
    import Listings from "../../lib/components/listings.svelte";
    import Footer from "$lib/components/footer.svelte";
</script>

<div class=" h-screen w-screen text-white bg-black-500 overflow-x-hidden">
    <Top />
    <Filter>
        <div
            slot="filterBtn"
            class=" flex flex-row justify-between items-end w-full"
        >
            <div class="flex flex-row gap-5">
                <FilterBtn />
                <FilterBtn />
                <FilterBtn />
                <FilterBtn />
            </div>
            <div class="flex flex-row items-center gap-3">
                <span class=" ">Sorting By :</span>
                <span
                    ><FilterBtn><span slot="text">Date added</span></FilterBtn
                    ></span
                >
            </div>
        </div>
    </Filter>
    <div class="flex flex-col items-center justify-center -mt-5 gap-5">
        <Listings />
        <Listings />
        <Listings />
        <Button />
    </div>
    <Footer color="bg-black-500" />
</div>
