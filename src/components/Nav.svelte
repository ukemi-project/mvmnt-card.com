<script>
  import { _, locale, locales } from "svelte-i18n";

  import RightsFlyoutMenu from "./RightsFlyoutMenu.svelte";

  export let open = false;
  export let segment;
</script>

<style>
  aside {
    /* offscreen by default */
    left: -100%;
    transition: left 0.3s ease-in-out;
  }

  .open {
    /* slide on screen */
    left: 0;
  }
</style>

<div class="z-40 -my-2 -mr-2 md:hidden">
  <button
    on:click={() => (open = !open)}
    type="button"
    class="flex flex-row items-center justify-between p-4 transition
    duration-150 ease-in-out rounded-md focus:outline-none">
    <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
      {#if !open}
        <svg
          fill="currentColor"
          viewBox="0 0 20 20"
          class="w-6 h-6 text-mcwhite">
          <path
            fill-rule="evenodd"
            d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0
            011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110
            2h-6a1 1 0 01-1-1z"
            clip-rule="evenodd" />
        </svg>
      {:else}
        <svg
          fill="currentColor"
          viewBox="0 0 20 20"
          class="w-6 h-6 text-mcblack">
          <path
            fill-rule="evenodd"
            d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414
            1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293
            4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
            clip-rule="evenodd" />
        </svg>
      {/if}
    </svg>
  </button>
</div>

<nav class="hidden space-x-10 md:flex {$_('direction')}" role="navigation">
  <a
    class="inline-flex items-center space-x-2 text-base font-medium leading-6
    transition duration-150 ease-in-out text-mcwhite hover:text-mcorange2"
    class:selected={segment === undefined}
    href=".">
    {$_('nav.home')}
  </a>
  <a
    class="inline-flex items-center space-x-2 text-base font-medium leading-6
    transition duration-150 ease-in-out text-mcwhite hover:text-mcorange2"
    class:selected={segment === 'about'}
    href="about">
    {$_('nav.about')}
  </a>
  <RightsFlyoutMenu />
  <a
    rel="prefetch"
    class="inline-flex items-center space-x-2 text-base font-medium leading-6
    transition duration-150 ease-in-out text-mcwhite hover:text-mcorange2"
    class:selected={segment === 'blog'}
    href="https://ukemi.ninja/blog">
    {$_('nav.blog')}
  </a>
  <span class="text-mcwhite">|</span>
  {#each $locales as item}
    <span
      class="inline-flex items-center space-x-2 text-base font-medium leading-6
      transition duration-150 ease-in-out text-mcwhite hover:text-mcorange2"
      class:selected={$locale.includes(item)}
      href={`#!${item}`}
      on:click={() => ($locale = item)}>
      {$_('languages.' + item.replace('-', '_'))}
    </span>
  {/each}
</nav>

<div class="items-center justify-end hidden space-x-8 md:flex md:flex-1 lg:w-0">
  <span class="inline-flex rounded-md shadow-sm">
    <a
      href="#"
      class="inline-flex items-center justify-center px-4 py-2 text-base
      font-medium leading-6 whitespace-no-wrap transition duration-150
      ease-in-out border border-transparent rounded-md bg-mcwhite text-mcblack
      hover:bg-mcorange2 hover:text-mcwhite focus:outline-none
      focus:border-mcwhite focus:shadow-outline-indigo active:bg-mcorange2">
      {$_('nav.cta')}
    </a>
  </span>
</div>

<!--
      Mobile menu, show/hide based on mobile menu state.

      Entering: "duration-200 ease-out"
        From: "opacity-0 scale-95"
        To: "opacity-100 scale-100"
      Leaving: "duration-100 ease-in"
        From: "opacity-100 scale-100"
        To: "opacity-0 scale-95"
    -->

<aside class="absolute w-full h-full bg-mcwhite" class:open>

  <nav class="w-full h-full p-12 text-xl bg-white">
    <a class="block" href="#about">About</a>
    <a class="block" href="#contact">Contact</a>
  </nav>
</aside>

<div
  class="absolute inset-x-0 top-0 z-10 invisible hidden p-2 transition
  origin-top-right transform">
  <div class="bg-white divide-y-2 rounded-lg shadow-xs divide-gray-50">
    <div class="z-20 px-5 pt-5 pb-6 space-y-6">
      <div class="flex items-center justify-between">
        <div>
          <img
            class="w-auto h-8"
            src="/img/logos/workflow-mark-on-white.svg"
            alt="Workflow" />
        </div>
        <div class="-mr-2">
          <button
            type="button"
            class="inline-flex items-center justify-center p-2 text-gray-400
            transition duration-150 ease-in-out rounded-md hover:text-gray-500
            hover:bg-gray-100 focus:outline-none focus:bg-gray-100
            focus:text-gray-500">
            <svg
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
      <div>
        <nav class="grid row-gap-8">
          <a
            href="#"
            class="flex items-center p-3 -m-3 space-x-3 transition duration-150
            ease-in-out rounded-md hover:bg-gray-50">
            <svg
              class="flex-shrink-0 w-6 h-6 text-yellow-600"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0
                002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2
                0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0
                01-2-2z" />
            </svg>
            <div class="text-base font-medium leading-6 text-gray-900">
              Analytics
            </div>
          </a>
          <a
            href="#"
            class="flex items-center p-3 -m-3 space-x-3 transition duration-150
            ease-in-out rounded-md hover:bg-gray-50">
            <svg
              class="flex-shrink-0 w-6 h-6 text-indigo-600"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777
                2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657
                5.656l-2.12 2.122" />
            </svg>
            <div class="text-base font-medium leading-6 text-gray-900">
              Engagement
            </div>
          </a>

        </nav>
      </div>
    </div>
  </div>
</div>
