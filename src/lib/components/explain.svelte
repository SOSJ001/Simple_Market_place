<script>
    import Button from "./button.svelte";
    import image from "../assets/image.png"

</script>

<div
    class=" md:px-20 md:py-20 py-10 md:grid md:grid-cols-2 flex flex-col gap-3 text-black-500"
>
    <div class="bg-gray-50 flex flex-col gap-20 justify-between py-10 px-5">
        <div>
            <span>It Startd with a Small idea</span>
            <span class=" flex-nowrap"
                >Lorem lorem lorem lorem lorem Lorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremvLorem lorem lorem lorem lorem
                Lorem lorem lorem lorem lorem Lorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremLorem lorem lorem lorem
                loremLorem lorem lorem lorem loremvLorem lorem lorem lorem lorem
                loremLorem lorem lorem lorem loremvLorem lorem lorem lorem lorem</span
            >
        </div>
        <div class="mt-3">
            <Button />
        </div>
    </div>
    <div class=" shadow-lg flex">
        <img src="{image}" alt="" class="w-full md:h-full h-1/2">
    </div>
</div>
