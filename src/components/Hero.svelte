<script>
  import { _, locale, locales } from "svelte-i18n";

  export let segment;
</script>

<div class="relative pt-6 pb-12 lg:pb-20 bg-mcblack">
  <div class="max-w-screen-xl px-4 mx-auto mt-10 sm:px-6 md:mt-16 lg:mt-20">
    <div class="text-center">
      <h2
        class="text-4xl font-extrabold leading-10 tracking-tight text-white sm:text-5xl sm:leading-none md:text-6xl">
        Movement Card
        <br />
        <span class="text-mcorange2">Right to the City</span>
      </h2>
      <p
        class="max-w-md mx-auto mt-3 text-base text-mcwhite sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
        A not-for-profit project that aims to help everyone understand their
        right to move.
      </p>
    </div>
  </div>
</div>
<div class="relative">
  <div class="absolute inset-0 flex flex-col">
    <div class="flex-1" />
    <div class="flex-1 w-full bg-gray-800" />
  </div>
  <div class="max-w-screen-xl px-4 mx-auto sm:px-6">
    <img
      class="relative rounded-lg shadow-lg"
      src="/img/component-images/top-nav-with-multi-column-layout-screenshot.png"
      alt="App screenshot" />
  </div>
</div>

<div class="bg-color4">
  <div
    class="max-w-screen-xl px-4 pt-16 pb-20 mx-auto sm:px-6 md:pb-24 lg:px-8">
    <h3
      class="text-sm font-semibold tracking-wide text-center text-gray-400 uppercase">
      Trusted by over 26,000 forward-thinking companies
    </h3>
    <div class="grid grid-cols-2 gap-8 mt-8 md:grid-cols-6 lg:grid-cols-5">
      <div class="flex justify-center col-span-1 md:col-span-2 lg:col-span-1">
        <img class="h-12" src="/img/logos/tuple-logo.svg" alt="Tuple" />
      </div>
      <div class="flex justify-center col-span-1 md:col-span-2 lg:col-span-1">
        <img class="h-12" src="/img/logos/mirage-logo.svg" alt="Mirage" />
      </div>
      <div class="flex justify-center col-span-1 md:col-span-2 lg:col-span-1">
        <img class="h-12" src="/img/logos/statickit-logo.svg" alt="StaticKit" />
      </div>
      <div class="flex justify-center col-span-1 md:col-span-3 lg:col-span-1">
        <img
          class="h-12"
          src="/img/logos/transistor-logo.svg"
          alt="Transistor" />
      </div>
      <div class="flex justify-center col-span-2 md:col-span-3 lg:col-span-1">
        <img
          class="h-12"
          src="/img/logos/workcation-logo.svg"
          alt="Workcation" />
      </div>
    </div>
  </div>
</div>
