<script>
  import Hero from "$lib/image-1.png";
    import Button from "./button.svelte";
</script>

<div class=" md:h-4/5  relative">
  <div
    class=" bg-cover bg-center md:h-full  w-full flex flex-col justify-end items-end p-5"
    style="background-image: url('{Hero}');"
  >
   
    <div
      class=" text-black flex flex-col gap-5 justify-between p-5 bg-gray-300 shadow-xl bg-opacity-20 md:w-1/2 md:h-4/5"
    >
      <div class="flex gap-5 flex-col font-medium">
        <div>
          <span class="text-3xl font-bold"
            >Luxury homeware for people <br /> who love timeless design quality</span
          >
        </div>
        <div>
          <span
            >With our new collection, view over 400 <br /> bespoke pieces from
            homeware through to <br /> furniture today</span
          >
        </div>
      </div>
      <Button/>
    </div>
  </div>
</div>
