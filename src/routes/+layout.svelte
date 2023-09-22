<script>
  import "../app.postcss";
  import {
    Tabs,
    Modal,
    TabItem    
  } from "flowbite-svelte";
  import Socials from "$lib/components/socials.svelte";
  // import { ArrowRightOutline } from "flowbite-svelte-icons";
  import Button from "$lib/components/button.svelte";
  let formModal = false
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


