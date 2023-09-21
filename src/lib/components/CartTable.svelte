<script>
    import Photo from "$lib/assets/Photo.png";
    import Rating from "$lib/components/rating.svelte";
    import QuanBtn from "$lib/components/QuanBtn.svelte";
    import Button from "$lib/components/button.svelte";
    export let successModal = false;
</script>

<div
    class=" bg-gray-500 flex items-center justify-center w-full text-white text-5xl md:p-10 p-2"
>
    <div
        class=" bg-black-500 md:p-10 p-2 md:w-4/5 w-full flex items-center justify-center"
    >
        <div class=" relative overflow-x-auto w-full pb-5">
            <table class="w-full text-sm text-white text-center">
                <thead class="text-xs text-white uppercase">
                    <tr class="">
                        <th scope="col" class=" text-start pb-5"> Product </th>
                        <th scope="col" class="pb-5 px-10"> Quantity </th>
                        <th scope="col" class="pb-5"> Total </th>
                    </tr>
                </thead>
                <tbody class="text-white">
                    <tr class="">
                        <th scope="row" class="font-medium">
                            <div class="flex fex-row gap-5">
                                <div class=" w-28">
                                    <img src={Photo} alt="photo" />
                                </div>
                                <div
                                    class="flex flex-col justify w-1/2 justify-center items-start gap-3"
                                >
                                    <div>Graystone vase</div>
                                    <div>
                                        A timeless ceramic vase with a tri color
                                        grey glaze.
                                    </div>
                                    <div class="flex flex-row gap-5">
                                        <span class="whitespace-nowrap"
                                            >Nle 399</span
                                        >
                                        <Rating />
                                    </div>
                                </div>
                            </div>
                        </th>
                        <td class=" flex justify-center"> <QuanBtn /> </td>
                        <td class=""> $2999 </td>
                    </tr>
                    <tr class="">
                        <th scope="row" class="font-medium">
                            <div class="flex fex-row gap-5">
                                <div class=" w-28">
                                    <img src={Photo} alt="photo" />
                                </div>
                                <div
                                    class="flex flex-col justify w-1/2 justify-center items-start gap-3"
                                >
                                    <div>Graystone vase</div>
                                    <div>
                                        A timeless ceramic vase with a tri color
                                        grey glaze.
                                    </div>
                                    <div class="flex flex-row gap-5">
                                        <span class="whitespace-nowrap"
                                            >Nle 399</span
                                        >
                                        <Rating />
                                    </div>
                                </div>
                            </div>
                        </th>
                        <td class=" flex justify-center"> <QuanBtn /> </td>
                        <td class=""> $2999 </td>
                    </tr>
                    <tr class="">
                        <th scope="row" class="font-medium">
                            <div class="flex fex-row gap-5">
                                <div class=" w-28">
                                    <img src={Photo} alt="photo" />
                                </div>
                                <div
                                    class="flex flex-col justify w-1/2 justify-center items-start gap-3"
                                >
                                    <div>Graystone vase</div>
                                    <div>
                                        A timeless ceramic vase with a tri color
                                        grey glaze.
                                    </div>
                                    <div class="flex flex-row gap-5">
                                        <span>Nle 399</span>
                                        <Rating />
                                    </div>
                                </div>
                            </div>
                        </th>
                        <td class=" flex justify-center"> <QuanBtn /> </td>

                        <td class=""> $2999 </td>
                    </tr>
                </tbody>
            </table>

            <div class="w-full text-sm p-5">
                <div class=" flex flex-col gap-3">
                    <div class="flex flex-row justify-between items-start">
                        <span class="font-medium text-left"
                            >Taxes and shipping are calculated at checkout</span
                        >
                        <div
                            class="flex flex-col justify-cente gap-3 items-center"
                        >
                            <div class="flex flex-row gap-20">
                                <span>Subtotal</span>
                                <span class="whitespace-nowrap">Nle 399</span>
                            </div>
                            <div class=" ">
                                <Button link="/">
                                    <span slot="text"> Go to checkout </span>
                                </Button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
