<script>
    import { Modal } from "flowbite-svelte";
    import Photo from "$lib/Photo.png";
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
                                <Button
                                    link="/"
                                    modal="true"
                                    bind:modalOpen={successModal}
                                    ;
                                >
                                    <span slot="text"> Go to checkout </span>
                                </Button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Success Modal below -->
    {#if successModal}
        <Modal
            bind:open={successModal}
            size="sm"
            autoclose={false}
            class="w-full bg-black-500 text-white pt-6 border-blue-600 border-2"
            color="blue"
        >
            <div
                class="flex flex-col justify-center items-center gap-5 w-full text-center text-sm"
            >
                <div>
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="84"
                        height="84"
                        viewBox="0 0 84 84"
                        fill="none"
                    >
                        <path
                            opacity="0.4"
                            d="M80.6649 38.3373V22.0278C80.6649 8.43651 75.2284 3 61.6371 3H45.3276C31.7363 3 26.2998 8.43651 26.2998 22.0278V26.2993H38.3378C51.9291 26.2993 57.3656 31.7358 57.3656 45.3271V57.3651H61.6371C75.2284 57.3651 80.6649 51.9286 80.6649 38.3373Z"
                            stroke="#00ADB5"
                            stroke-width="5.82483"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        />
                        <path
                            d="M57.3651 61.6366V45.3271C57.3651 31.7358 51.9286 26.2993 38.3373 26.2993H22.0278C8.43651 26.2993 3 31.7358 3 45.3271V61.6366C3 75.2279 8.43651 80.6644 22.0278 80.6644H38.3373C51.9286 80.6644 57.3651 75.2279 57.3651 61.6366Z"
                            stroke="#00ADB5"
                            stroke-width="5.82483"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        />
                        <path
                            d="M18.8438 53.4811L26.416 61.0534L41.5218 45.9088"
                            stroke="#EEEEEE"
                            stroke-width="5.82483"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        />
                    </svg>
                </div>
                <span
                    class="px-5 py-3 rounded-full bg-blue-600 font-medium w-4/5"
                    >Checkout Successful</span
                >
            </div>
        </Modal>
    {/if}
</div>
