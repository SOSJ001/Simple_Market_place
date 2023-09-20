<script>
    import Button from "./button.svelte";
    import image from "../assets/Photo.png";
    import Rating from "./rating.svelte";
    import QuanBtn from "./QuanBtn.svelte";
    let link = "/payment";
</script>

<div
    class=" relative bg-gray-500 md:px-20 md:py-10 py-5 md:grid md:grid-cols-2 flex flex-col gap-3 items-center text-black-500"
>
    <div class=" shadow-lg w-full flex justify-center items-center">
        <img src={image} alt="" class=" bg-cover w-full"/>
        <!-- <span>hi</span> -->
    </div>
    <div class="flex flex-col gap-3 justify-between py-5 px-5 text-white">
        <div class="flex flex-col gap-3">
            <span class="font-medium text-2xl">The Dany Chair</span>

            <span class="text-sm">Nle 399</span>
            <Rating />
            <span class="text-md font-semibold">Product Description</span>
            <span class=" flex-nowrap"
                >Lorem lorem lorem lorem lorem Lorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremvLorem lorem lorem lorem lorem
                Lorem lorem lorem lorem lorem Lorem lorem lorem lorem loremLorem
            </span>
            <span class="text-md font-semibold">Dimension</span>
            <div class="flex flex-row gap-10">
                <div class=" flex flex-col">
                    <span>Height</span>
                    <span>110cm</span>
                </div>
                <div class=" flex flex-col">
                    <span>Height</span>
                    <span>110cm</span>
                </div>
                <div class=" flex flex-col">
                    <span>Height</span>
                    <span>110cm</span>
                </div>
            </div>
            <span class="text-md font-semibold">Quantity</span>
            <QuanBtn />
            <div class="flex flex-row gap-10 text-black-500">
                <Button link={link}>
                    <span slot="text"> Add to cart </span>
                </Button>
                <Button>
                    <span slot="text"> Save to favourite </span>
                </Button>
            </div>
        </div>
    </div>
</div>
