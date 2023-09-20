<script>
    import Large from "../assets/Large.png";
</script>

<div
    class="w-full h-2/5 bg-cover flex flex-col items-start justify-center p-10 gap-5 text-black-500 font-medium"
    style="background-image: url('{Large}');"
>
    <span class="text-2xl">All products</span>
    <div class=" w-full">
        <slot name="filterBtn">
            <div>
                texting
            </div>
        </slot>
    </div>

</div>
