<script>
    import Large from "../assets/Large.png";
    import Button from "./button.svelte";
</script>

<div
    class="w-full h-4/6 bg-cover flex items-center justify-center"
    style="background-image: url('{Large}');"
>
    <div
        class="text-center bg-gray-50 h-full md:w-1/2 w-4/5 bg-opacity-25 shadow-lg gap-5 flex flex-col  justify-center items-center md:p-10 p-5"
    >
        <span class="md:text-3xl text-lg font-semibold">
            Join the club and get the benefits</span
        >
        <span class="w-2/3 text-center md:text-lg text-sm   ">
            Sign up for our newsletter and receive exclusive offers on new
            ranges, sales, pop up stores and more
        </span>
        <div class="flex flex-row justify-between md:w-2/3 w-full font-semibold md:text-lg text-sm ">
            <div class="flex flex-row items-center md:gap-5 gap-2">
                <slot name="checkbox1">
                    <input type="checkbox" />
                </slot>
                <div class="flex flex-col gap-1">
                    <span>Exclusive</span>
                    <span>Offers</span>
                </div>
            </div>
            <div class="flex flex-row items-center md:gap-5 gap-2">
                <slot name="checkbox2">
                    <input type="checkbox" />
                </slot>
                <div class="flex flex-col gap-1">
                    <span>Free</span>
                    <span>Events</span>
                </div>
            </div>
            <div class="flex flex-row items-center md:gap-5 gap-2">
                <slot name="checkbox3">
                    <input type="checkbox" />
                </slot>
                <div class="flex flex-col gap-1">
                    <span>Large</span>
                    <span>Discounts</span>
                </div>
            </div>
        </div>
        <div class=" w-full">
            <form action="">
               <div class="flex justify-center w-full">
                <input type="text" id="first_name" class="bg-black-500 border border-gray-500 text-md  focus:ring-gray-500 focus:border-blue-600 block w-4/6 p-2.5 placeholder-gray-400  " placeholder="michaelsosj@gmail.com">
                <button class=" hover:bg-blue-700 font-semibold bg-blue-500 p-3">Sign Up</button>
                <!-- <Button>
                    <span slot="text">
                        Signup
                    </span>
                </Button> -->
               </div> 
            </form>
        </div>
    </div>
</div>
