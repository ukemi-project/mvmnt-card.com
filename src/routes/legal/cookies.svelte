<script>
  import { _, locale } from "svelte-i18n";
  import getArrayFromLocale from "../../utils/getArrayFromLocale";
  $: content = getArrayFromLocale("cookies.content", $locale);
</script>

<svelte:head>
  <title>{$_('cookies.title')} | Movement Card</title>
</svelte:head>

<section
  id="cookies"
  class="px-4 py-16 overflow-hidden bg-white xl:py-36 sm:px-6 lg:px-8">
  <div class="mx-auto max-w-max-content lg:max-w-5xl">
    <div class="relative z-10 mb-8 md:mb-2 md:px-6">
      <div class="text-base max-w-prose lg:max-w-none">
        <h1
          class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-mcblack sm:text-5xl sm:leading-10">
          {$_('cookies.title')}
        </h1>

        <hr class="my-8 border-t-0 border-b-2 border-mcorange2" />

        {#each content as { title, html }}
          <h2 class="mt-8 text-xl font-semibold leading-6 tracking-wide">
            {title}
          </h2>
          <p class="my-4">
            {@html html}
          </p>
        {/each}
      </div>
    </div>
  </div>
</section>
