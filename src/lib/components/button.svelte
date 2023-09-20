<script>
    export let link = "/browsing";
     
</script>
<div>
    <a href="{link}" >
    <button
        class="bg-blue-600 p-3 mb-3 rounded-lg font-semibold hover:bg-blue-700"
    >
        <slot name="text">
            VIEW COLLECTION
        </slot>
    </button>
</a>
</div>