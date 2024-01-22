<script>
    import Chair from "$lib/Photo.png";
    import Rating from "./rating.svelte";
</script>

<a href="/ProductDetails" class="hover:text-blue-500 text-gray-50">
    <div class="  flex flex-col md:gap-3 gap-1 items-center justify-center">
        <div class=" md:w-52 w-24 flex items-center justify-center">
            <!-- image -->
            <slot name="image">
                <img src={Chair} alt="Chair" />
            </slot>
        </div>
        <Rating/>

        <div>
            <!-- text -->
            Desccription here
        </div>
    </div>
</a>
