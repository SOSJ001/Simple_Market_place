<script>
    export let link = "/browsing";
    export let width = "w-auto";
    export let round = "rounded-lg";
</script>

<div class="flex w-full justify-center items-center">
    <a href={link} class={width}>
        <button
            class="bg-blue-600 p-3 mb-3 {round} font-semibold hover:bg-blue-700 w-full"
        >
            <slot name="text">VIEW COLLECTION</slot>
        </button>
    </a>
</div>
