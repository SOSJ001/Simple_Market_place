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
                        fill="#EEEEEE"
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
            ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="27"
                height="26"
                viewBox="0 0 27 26"
                fill="none"
            >
                <path
                    d="M9.61339 25.0588C10.5648 25.0588 11.3361 24.2875 11.3361 23.3361C11.3361 22.3847 10.5648 21.6134 9.61339 21.6134C8.66198 21.6134 7.89071 22.3847 7.89071 23.3361C7.89071 24.2875 8.66198 25.0588 9.61339 25.0588Z"
                    fill="#EEEEEE"
                />
                <path
                    d="M21.6721 25.0588C22.6236 25.0588 23.3948 24.2875 23.3948 23.3361C23.3948 22.3847 22.6236 21.6134 21.6721 21.6134C20.7207 21.6134 19.9495 22.3847 19.9495 23.3361C19.9495 24.2875 20.7207 25.0588 21.6721 25.0588Z"
                    fill="#EEEEEE"
                />
                <path
                    d="M25.1175 5.24797H6.01299L5.3067 1.63035C5.26643 1.43286 5.15818 1.25575 5.0008 1.12985C4.84342 1.00394 4.64686 0.937213 4.44536 0.941276H1V2.66395H3.73906L7.02938 19.2017C7.06964 19.3992 7.17789 19.5763 7.33527 19.7022C7.49266 19.8281 7.68921 19.8948 7.89071 19.8907H23.3948V18.1681H8.59701L7.89071 14.7227H23.3948C23.5939 14.7276 23.7886 14.6633 23.9456 14.5408C24.1027 14.4183 24.2124 14.2452 24.2562 14.0509L25.9788 6.29881C26.0077 6.17101 26.007 6.0383 25.9769 5.9108C25.9467 5.7833 25.8879 5.66436 25.8048 5.56302C25.7218 5.4617 25.6167 5.38065 25.4976 5.32605C25.3785 5.27146 25.2485 5.24475 25.1175 5.24797ZM22.7057 13H7.56341L6.35753 6.97065H24.0408L22.7057 13Z"
                    fill="#EEEEEE"
                />
                <path
                    d="M9.61339 25.0588C10.5648 25.0588 11.3361 24.2875 11.3361 23.3361C11.3361 22.3847 10.5648 21.6134 9.61339 21.6134C8.66198 21.6134 7.89071 22.3847 7.89071 23.3361C7.89071 24.2875 8.66198 25.0588 9.61339 25.0588Z"
                    stroke="#EEEEEE"
                />
                <path
                    d="M21.6721 25.0588C22.6236 25.0588 23.3948 24.2875 23.3948 23.3361C23.3948 22.3847 22.6236 21.6134 21.6721 21.6134C20.7207 21.6134 19.9495 22.3847 19.9495 23.3361C19.9495 24.2875 20.7207 25.0588 21.6721 25.0588Z"
                    stroke="#EEEEEE"
                />
                <path
                    d="M25.1175 5.24797H6.01299L5.3067 1.63035C5.26643 1.43286 5.15818 1.25575 5.0008 1.12985C4.84342 1.00394 4.64686 0.937213 4.44536 0.941276H1V2.66395H3.73906L7.02938 19.2017C7.06964 19.3992 7.17789 19.5763 7.33527 19.7022C7.49266 19.8281 7.68921 19.8948 7.89071 19.8907H23.3948V18.1681H8.59701L7.89071 14.7227H23.3948C23.5939 14.7276 23.7886 14.6633 23.9456 14.5408C24.1027 14.4183 24.2124 14.2452 24.2562 14.0509L25.9788 6.29881C26.0077 6.17101 26.007 6.0383 25.9769 5.9108C25.9467 5.7833 25.8879 5.66436 25.8048 5.56302C25.7218 5.4617 25.6167 5.38065 25.4976 5.32605C25.3785 5.27146 25.2485 5.24475 25.1175 5.24797ZM22.7057 13H7.56341L6.35753 6.97065H24.0408L22.7057 13Z"
                    stroke="#EEEEEE"
                />
            </svg><span>Cart</span></a
        >

        <!-- Profile Svg -->
        <a
            class="flex gap-1"
            on:click|preventDefault={() => {
                formModal = !formModal;
            }}
            href="/"
            ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="27"
                height="26"
                viewBox="0 0 27 26"
                fill="none"
            >
                <path
                    d="M13.5 5.85714C12.6171 5.85714 11.7539 6.11897 11.0198 6.60951C10.2856 7.10005 9.71343 7.79728 9.37554 8.61302C9.03765 9.42876 8.94924 10.3264 9.1215 11.1924C9.29375 12.0584 9.71894 12.8538 10.3433 13.4782C10.9676 14.1025 11.7631 14.5277 12.6291 14.6999C13.4951 14.8722 14.3927 14.7838 15.2084 14.4459C16.0242 14.108 16.7214 13.5358 17.2119 12.8017C17.7025 12.0675 17.9643 11.2044 17.9643 10.3214C17.9643 9.13742 17.4939 8.00192 16.6567 7.1647C15.8195 6.32748 14.684 5.85714 13.5 5.85714ZM13.5 13C12.9702 13 12.4524 12.8429 12.0119 12.5486C11.5714 12.2543 11.2281 11.8359 11.0253 11.3465C10.8226 10.857 10.7695 10.3185 10.8729 9.79886C10.9763 9.27927 11.2314 8.802 11.606 8.42739C11.9806 8.05279 12.4578 7.79768 12.9774 7.69432C13.497 7.59097 14.0356 7.64401 14.525 7.84675C15.0145 8.04948 15.4328 8.3928 15.7272 8.83329C16.0215 9.27378 16.1786 9.79166 16.1786 10.3214C16.1778 11.0316 15.8953 11.7124 15.3932 12.2146C14.891 12.7167 14.2102 12.9992 13.5 13Z"
                    fill="#EEEEEE"
                />
                <path
                    d="M13.5 0.5C11.0277 0.5 8.61099 1.23311 6.55538 2.60663C4.49976 3.98015 2.89761 5.93238 1.95151 8.21646C1.00542 10.5005 0.757874 13.0139 1.24019 15.4386C1.7225 17.8634 2.91301 20.0907 4.66117 21.8388C6.40933 23.587 8.63661 24.7775 11.0614 25.2598C13.4861 25.7421 15.9995 25.4946 18.2835 24.5485C20.5676 23.6024 22.5199 22.0002 23.8934 19.9446C25.2669 17.889 26 15.4723 26 13C25.9963 9.68594 24.6781 6.50868 22.3347 4.16529C19.9913 1.82189 16.8141 0.503734 13.5 0.5ZM8.14286 22.2647V21.0357C8.14364 20.3255 8.4261 19.6447 8.92826 19.1425C9.43042 18.6404 10.1113 18.3579 10.8214 18.3571H16.1786C16.8887 18.3579 17.5696 18.6404 18.0717 19.1425C18.5739 19.6447 18.8564 20.3255 18.8571 21.0357V22.2647C17.2314 23.214 15.3826 23.7143 13.5 23.7143C11.6174 23.7143 9.7686 23.214 8.14286 22.2647ZM20.6362 20.9695C20.6184 19.7983 20.1412 18.6809 19.3074 17.8582C18.4736 17.0356 17.3499 16.5734 16.1786 16.5714H10.8214C9.65009 16.5734 8.52643 17.0356 7.69261 17.8582C6.8588 18.6809 6.38159 19.7983 6.36384 20.9695C4.7447 19.5237 3.60289 17.6202 3.08959 15.5111C2.57629 13.402 2.71572 11.1867 3.48941 9.15862C4.26311 7.13051 5.63458 5.38524 7.42221 4.1539C9.20985 2.92256 11.3293 2.26324 13.5 2.26324C15.6707 2.26324 17.7902 2.92256 19.5778 4.1539C21.3654 5.38524 22.7369 7.13051 23.5106 9.15862C24.2843 11.1867 24.4237 13.402 23.9104 15.5111C23.3971 17.6202 22.2553 19.5237 20.6362 20.9695Z"
                    fill="#EEEEEE"
                />
                <path
                    d="M13.5 5.85714C12.6171 5.85714 11.7539 6.11897 11.0198 6.60951C10.2856 7.10005 9.71343 7.79728 9.37554 8.61302C9.03765 9.42876 8.94924 10.3264 9.1215 11.1924C9.29375 12.0584 9.71894 12.8538 10.3433 13.4782C10.9676 14.1025 11.7631 14.5277 12.6291 14.6999C13.4951 14.8722 14.3927 14.7838 15.2084 14.4459C16.0242 14.108 16.7214 13.5358 17.2119 12.8017C17.7025 12.0675 17.9643 11.2044 17.9643 10.3214C17.9643 9.13742 17.4939 8.00192 16.6567 7.1647C15.8195 6.32748 14.684 5.85714 13.5 5.85714ZM13.5 13C12.9702 13 12.4524 12.8429 12.0119 12.5486C11.5714 12.2543 11.2281 11.8359 11.0253 11.3465C10.8226 10.857 10.7695 10.3185 10.8729 9.79886C10.9763 9.27927 11.2314 8.802 11.606 8.42739C11.9806 8.05279 12.4578 7.79768 12.9774 7.69432C13.497 7.59097 14.0356 7.64401 14.525 7.84675C15.0145 8.04948 15.4328 8.3928 15.7272 8.83329C16.0215 9.27378 16.1786 9.79166 16.1786 10.3214C16.1778 11.0316 15.8953 11.7124 15.3932 12.2146C14.891 12.7167 14.2102 12.9992 13.5 13Z"
                    stroke="#EEEEEE"
                />
                <path
                    d="M13.5 0.5C11.0277 0.5 8.61099 1.23311 6.55538 2.60663C4.49976 3.98015 2.89761 5.93238 1.95151 8.21646C1.00542 10.5005 0.757874 13.0139 1.24019 15.4386C1.7225 17.8634 2.91301 20.0907 4.66117 21.8388C6.40933 23.587 8.63661 24.7775 11.0614 25.2598C13.4861 25.7421 15.9995 25.4946 18.2835 24.5485C20.5676 23.6024 22.5199 22.0002 23.8934 19.9446C25.2669 17.889 26 15.4723 26 13C25.9963 9.68594 24.6781 6.50868 22.3347 4.16529C19.9913 1.82189 16.8141 0.503734 13.5 0.5ZM8.14286 22.2647V21.0357C8.14364 20.3255 8.4261 19.6447 8.92826 19.1425C9.43042 18.6404 10.1113 18.3579 10.8214 18.3571H16.1786C16.8887 18.3579 17.5696 18.6404 18.0717 19.1425C18.5739 19.6447 18.8564 20.3255 18.8571 21.0357V22.2647C17.2314 23.214 15.3826 23.7143 13.5 23.7143C11.6174 23.7143 9.7686 23.214 8.14286 22.2647ZM20.6362 20.9695C20.6184 19.7983 20.1412 18.6809 19.3074 17.8582C18.4736 17.0356 17.3499 16.5734 16.1786 16.5714H10.8214C9.65009 16.5734 8.52643 17.0356 7.69261 17.8582C6.8588 18.6809 6.38159 19.7983 6.36384 20.9695C4.7447 19.5237 3.60289 17.6202 3.08959 15.5111C2.57629 13.402 2.71572 11.1867 3.48941 9.15862C4.26311 7.13051 5.63458 5.38524 7.42221 4.1539C9.20985 2.92256 11.3293 2.26324 13.5 2.26324C15.6707 2.26324 17.7902 2.92256 19.5778 4.1539C21.3654 5.38524 22.7369 7.13051 23.5106 9.15862C24.2843 11.1867 24.4237 13.402 23.9104 15.5111C23.3971 17.6202 22.2553 19.5237 20.6362 20.9695Z"
                    stroke="#EEEEEE"
                />
            </svg>Profile</a
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
