<script>
  import "../app.postcss";
  import { Modal, Tabs, TabItem } from "flowbite-svelte";
  import Socials from "$lib/components/socials.svelte";
  import Button from "$lib/components/button.svelte";
  let formModal = false;
  let successModal = false;
</script>

<slot />
<!-- signup and login modals below -->
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
      <div class="flex flex-col gap-5 justify-center items-center">
        <Socials />
        <div class="w-4/5 flex flex-col gap-5 justify-center items-center">
          <div class="flex flex-row justify-between items-center gap-10">
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
          <div class="flex flex-row justify-between items-center gap-10">
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
      <div class="flex flex-col gap-5 justify-center items-center">
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

<!-- Success Modal below -->
<Modal
  bind:open={successModal}
  size="sm"
  autoclose={false}
  class="w-full bg-black-500 text-white pt-6 border-blue-600 border-2"
  color="blue"
>
  <div
    class="flex flex-col justify-center items-center gap-5 w-full text-center"
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
    <span class="px-5 py-3 rounded-full bg-blue-600 font-medium w-4/5"
      >Checkout Successful</span
    >
  </div>
</Modal>
