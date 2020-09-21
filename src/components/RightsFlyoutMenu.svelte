<script>
  import { _, locale, locales } from "svelte-i18n";

  export let open = false;
  export let segment;
</script>

<style>
  .open {
    visibility: visible;
  }
</style>

<div class="relative">
  <button
    type="a"
    class="inline-flex items-center space-x-2 text-base font-medium leading-6 transition duration-150 ease-in-out text-mcwhite hover:text-mcorange2"
    class:open
    on:click={() => (open = !open)}
    class:selected={segment === 'rights'}>

    <span>{$_('nav.rights')}</span>
    <svg
      class="w-5 h-5 text-gray-400 transition duration-150 ease-in-out group-hover:text-gray-500 group-focus:text-gray-500"
      fill="currentColor"
      viewBox="0 0 20 20">
      <path
        fill-rule="evenodd"
        d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414
        1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
        clip-rule="evenodd" />
    </svg>
  </button>

  <!--
    Flyout menu, show/hide based on flyout menu state.

    Entering: "transition ease-out duration-200"
      From: "opacity-0 translate-y-1"
      To: "opacity-100 translate-y-0"
    Leaving: "transition ease-in duration-150"
      From: "opacity-100 translate-y-0"
      To: "opacity-0 translate-y-1"
  -->
  <div
    class="absolute z-40 invisible w-screen max-w-md px-2 mt-3 transform -translate-x-1/2 left-1/2 sm:px-0 lg:max-w-xl"
    class:open>
    <div class="rounded-lg shadow-lg">
      <div class="overflow-hidden rounded-lg shadow-xs">
        <div
          class="relative z-20 grid gap-6 px-5 py-6 bg-white sm:gap-8 sm:p-8 lg:grid-cols-2">
          <a
            on:click={() => (open = !open)}
            href="sct"
            class="flex items-start p-3 -m-3 space-x-4 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <div
              class="flex items-center justify-center flex-shrink-0 w-12 h-12 rounded-md sm:h-16 sm:w-16 ">
              <img class="" src="flags/gb-sct.svg" alt="Scotland Flag" />
            </div>
            <div
              class="flex items-center justify-center h-12 space-y-1 sm:h-16">
              <p
                class="self-center flex-1 text-base font-medium leading-6 text-gray-900">
                Scotland (SCT)
              </p>
            </div>
          </a>
          <a
            on:click={() => (open = !open)}
            href="fi"
            class="flex items-start p-3 -m-3 space-x-4 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <div
              class="flex items-center justify-center flex-shrink-0 w-12 h-12 rounded-md sm:h-16 sm:w-16 ">
              <img class="" src="flags/fi.svg" alt="Finland Flag" />
            </div>
            <div
              class="flex items-center justify-center h-12 space-y-1 sm:h-16">
              <p
                class="self-center flex-1 text-base font-medium leading-6 text-gray-900">
                Finland (FI)
              </p>
            </div>
          </a>
          <a
            on:click={() => (open = !open)}
            href="nz"
            class="flex items-start p-3 -m-3 space-x-4 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <div
              class="flex items-center justify-center flex-shrink-0 w-12 h-12 rounded-md sm:h-16 sm:w-16 ">
              <img class="" src="flags/nz.svg" alt="New Zealand Flag" />
            </div>
            <div
              class="flex items-center justify-center h-12 space-y-1 sm:h-16">
              <p
                class="self-center flex-1 text-base font-medium leading-6 text-gray-900">
                New Zealand (NZ)
              </p>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</div>
