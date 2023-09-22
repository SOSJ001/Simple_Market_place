<script>
    import { Tabs, Modal, TabItem } from "flowbite-svelte";
    import Socials from "$lib/components/socials.svelte";
    // import { ArrowRightOutline } from "flowbite-svelte-icons";
    import Button from "$lib/components/button.svelte";
    import { fade } from "svelte/transition";
    let formModal = false;
    let addModal = false;
    //   let successModal = false;
</script>

<!-- top below -->
<div
    class="p-5 md:grid md:grid-cols-3 md:gap-0 gap-3 flex flex-row justify-between items-center text-white font-semibold"
>
    <a href="/"><div class=" text-2xl">S.O.S</div></a>

    <div class="relative">
        <input
            type="text"
            id="email-address-icon"
            class=" border text-gray-50 text-sm rounded-lg block w-full pr-10 p-2.5 bg-gray-500 border-gray-600 placeholder-gray-50 focus:ring-white focus:border-white"
            placeholder="Search Here"
        />
        <div class="absolute inset-y-0 right-0 flex items-center pr-3.5">
            <button>
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="23"
                    height="23"
                    viewBox="0 0 23 23"
                    fill="none"
                >
                    <path
                        d="M22 20.9016L16.1338 15.0354C17.5434 13.3431 18.2463 11.1726 18.0963 8.97523C17.9463 6.7779 16.955 4.72299 15.3285 3.23797C13.702 1.75296 11.5656 0.952175 9.36368 1.00221C7.1618 1.05225 5.06398 1.94925 3.50661 3.50661C1.94925 5.06398 1.05225 7.1618 1.00221 9.36368C0.952175 11.5656 1.75296 13.702 3.23797 15.3285C4.72299 16.955 6.7779 17.9463 8.97523 18.0963C11.1726 18.2463 13.3431 17.5434 15.0354 16.1338L20.9016 22L22 20.9016ZM2.58101 9.57185C2.58101 8.18919 2.99102 6.83758 3.75918 5.68795C4.52734 4.53831 5.61916 3.64228 6.89657 3.11316C8.17398 2.58404 9.5796 2.4456 10.9357 2.71534C12.2918 2.98508 13.5374 3.65089 14.5151 4.62858C15.4928 5.60627 16.1586 6.85191 16.4284 8.208C16.6981 9.56409 16.5597 10.9697 16.0305 12.2471C15.5014 13.5245 14.6054 14.6164 13.4557 15.3845C12.3061 16.1527 10.9545 16.5627 9.57185 16.5627C7.71839 16.5606 5.94144 15.8234 4.63085 14.5128C3.32026 13.2023 2.58307 11.4253 2.58101 9.57185Z"
                        
                        stroke="#EEEEEE"
                    />
                </svg>
            </button>
        </div>
    </div>

    <div class="flex flex-row md:gap-10 gap-3 justify-end">
        <!-- add button -->

        <a
            class="flex gap-1"
            on:click|preventDefault={() => {
                addModal = !addModal;
            }}
            href="/"
            ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="27"
                height="26"
                viewBox="0 0 20 20"
                ><path
                    fill="currentColor"
                    d="M11 9h4v2h-4v4H9v-4H5V9h4V5h2v4zm-1 11a10 10 0 1 1 0-20a10 10 0 0 1 0 20zm0-2a8 8 0 1 0 0-16a8 8 0 0 0 0 16z"
                /></svg
            ><span>Add</span></a
        >

        <!-- Cart svg -->
        <a class="flex gap-1" href="/payment"
            ><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M0 1h4.764l.545 2h18.078l-3.666 11H7.78l-.5 2H22v2H4.72l1.246-4.989L3.236 3H0V1Zm7.764 11h10.515l2.334-7H5.855l1.909 7ZM4 21a2 2 0 1 1 4 0a2 2 0 0 1-4 0Zm14 0a2 2 0 1 1 4 0a2 2 0 0 1-4 0Z"/></svg><span>Cart</span></a
        >

        <!-- Profile Svg -->
        <a
            class="flex gap-1"
            on:click|preventDefault={() => {
                formModal = !formModal;
            }}
            href="/"
            ><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 16 16"><path fill="currentColor" fill-rule="evenodd" d="M8 14.5a6.47 6.47 0 0 0 3.25-.87V11.5A2.25 2.25 0 0 0 9 9.25H7a2.25 2.25 0 0 0-2.25 2.25v2.13A6.47 6.47 0 0 0 8 14.5Zm4.75-3v.937a6.5 6.5 0 1 0-9.5 0V11.5a3.752 3.752 0 0 1 2.486-3.532a3 3 0 1 1 4.528 0A3.752 3.752 0 0 1 12.75 11.5ZM8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16ZM9.5 6a1.5 1.5 0 1 1-3 0a1.5 1.5 0 0 1 3 0Z" clip-rule="evenodd"/></svg>Profile</a
        >
    </div>
</div>
<!-- signup and login modals below -->
{#if formModal}
    <div transition:fade>
        <Modal
            bind:open={formModal}
            size="md"
            autoclose={false}
            class="w-full bg-black-500 text-white pt-6"
            color="blue"
        >
            <Tabs
                style="full"
                contentClass="bg-black-500 text-white w-full"
                defaultClass="flex rounded-lg divide-x divide-blue-600 shadow"
            >
                <!-- Signup tab here below -->

                <TabItem
                    class="w-full"
                    activeClasses=" text-white p-4  w-full border-t border-l border-blue-600"
                    inactiveClasses=" bg-blue-600 text-white p-4 w-full "
                    open
                >
                    <span slot="title">Sign Up</span>
                    <div
                        class="flex flex-col gap-5 justify-center items-center"
                    >
                        <Socials />
                        <div
                            class="w-4/5 flex flex-col gap-5 justify-center items-center"
                        >
                            <div
                                class="flex flex-row justify-between items-center gap-10"
                            >
                                <div class=" space-y-2">
                                    <label for="Fname">First Name</label>
                                    <input
                                        id="Fname"
                                        type="text"
                                        class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                                    />
                                </div>
                                <div class=" space-y-2">
                                    <label for="Lname">Last Name</label>
                                    <input
                                        id="Lname"
                                        type="text"
                                        class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                                    />
                                </div>
                            </div>
                            <div
                                class="flex flex-row justify-between items-center gap-10"
                            >
                                <div class=" space-y-2">
                                    <label for="Fname">First Name</label>
                                    <input
                                        id="Fname"
                                        type="text"
                                        class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                                    />
                                </div>
                                <div class=" space-y-2">
                                    <label for="Lname">Last Name</label>
                                    <input
                                        id="Lname"
                                        type="text"
                                        class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                                    />
                                </div>
                            </div>
                            <Button width="w-full" round="rounded-full">
                                <span slot="text"> Sign Up </span>
                            </Button>
                        </div>
                    </div>
                </TabItem>

                <!-- Login tab here below -->

                <TabItem
                    class="w-full"
                    activeClasses=" text-white p-4 border-t border-l border-blue-600 w-full"
                    inactiveClasses="bg-blue-600 text-white p-4 w-full"
                >
                    <span slot="title">Log in</span>
                    <div
                        class="flex flex-col gap-5 justify-center items-center"
                    >
                        <Socials><span slot="text">Log in</span></Socials>
                        <div class=" space-y-2 w-4/5">
                            <label for="Fname">Email address</label>
                            <input
                                id="Fname"
                                type="text"
                                class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                            />
                        </div>

                        <div class=" space-y-2 w-4/5">
                            <label for="Fname">Password</label>
                            <input
                                id="Fname"
                                type="password"
                                class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                            />
                        </div>

                        <Button width="w-4/5" round="rounded-full">
                            <span slot="text"> Log in </span>
                        </Button>
                    </div>
                </TabItem>
            </Tabs>
        </Modal>
    </div>
{/if}

<!-- add product listings modals -->
{#if addModal}
    <div transition:fade>
        <Modal
            bind:open={addModal}
            size="md"
            autoclose={false}
            class="w-full bg-black-500 text-white pt-6"
            color="blue"
        >
        <div
            class="flex flex-col gap-5 justify-center items-center"
        >
        <span class="font-medium text-2xl">Add Product Listings</span>

            <div
                class="w-4/5 flex flex-col gap-5 justify-center items-center"
            >
                <div
                    class="flex flex-row justify-between items-center gap-10"
                >
                    <div class=" space-y-2">
                        <label for="Fname">Product Name</label>
                        <input
                            id="Fname"
                            type="text"
                            class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                        />
                    </div>
                    <div class=" space-y-2">
                        <label for="Lname">Product Price</label>
                        <input
                        min="1"
                            id="Lname"
                            type="number"
                            class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                        />
                    </div>
                </div>
                <div
                    class="flex flex-row justify-between items-center gap-10"
                >
                    <div class=" space-y-2">
                        <label for="Fname">Image</label>
                        <input
                            id="Fname"
                            type="file"
                            class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                        />
                    </div>
                    <div class=" space-y-2">
                        <label for="Lname">Description</label>
                        <input
                            id="Lname"
                            type="text"
                            class=" border-4 border-gray-500 w-full rounded-lg bg-black-500"
                        />
                    </div>
                </div>
                <Button width="w-full" round="rounded-full" link="/ProductDetails" >
                    <span slot="text"> Add Listings </span>
                </Button>
            </div>
        </Modal>
    </div>
{/if}
<style>
    a:hover{
        color: aqua;
    }
</style>