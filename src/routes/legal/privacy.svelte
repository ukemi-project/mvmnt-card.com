<script>
  import { _, locale } from "svelte-i18n";
  import getArrayFromLocale from "../../utils/getArrayFromLocale";

  $: definitions = getArrayFromLocale(
    "privacy-policy.definitions.articles",
    $locale
  );

  $: personalDataCollected = getArrayFromLocale(
    "privacy-policy.personal-data.collection.sources",
    $locale
  );
</script>

<svelte:head>
  <title>{$_('privacy-policy.title')} | Movement Card</title>
</svelte:head>
<section
  id="privacy"
  class="px-4 py-16 overflow-hidden bg-white xl:py-36 sm:px-6 lg:px-8">
  <div class="mx-auto max-w-max-content lg:max-w-5xl">
    <div class="relative z-10 mb-8 md:mb-2 md:px-6">
      <div class="text-base max-w-prose lg:max-w-none">
        <h1
          class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-mcblack sm:text-5xl sm:leading-10">
          {$_('privacy-policy.title')}
        </h1>
        <p
          class="mt-5 mb-2 font-semibold leading-6 tracking-wide uppercase text-mcorange2">
          {$_('privacy-policy.subtitle')}
        </p>
        <small>{$_('privacy-policy.last-updated')}</small>
        <p class="my-4">{$_('privacy-policy.intro')}</p>
        <p class="my-4">
          {@html $_('privacy-policy.email')}
        </p>

        <hr class="my-8 border-b-2 border-gray-200" />

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.scope.title')}
        </h2>

        <p class="my-4">{$_('privacy-policy.scope.copy')}</p>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.personal-data.meaning.title')}
        </h2>
        <p class="my-4">{$_('privacy-policy.personal-data.meaning.copy')}</p>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.personal-data.collection.title')}
        </h2>
        <p class="my-4">{$_('privacy-policy.personal-data.collection.copy')}</p>

        <ol class="ml-8 list-decimal">
          {#each personalDataCollected as source}
            <li class="my-4">
              {source.title}
              <ol class="ml-8 list-disc">
                {#each Array(Object.keys(source).length - 1) as _, i}
                  <li class="">{source[`list.${i}`]}</li>
                {/each}
              </ol>
            </li>
          {/each}
        </ol>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.personal-data.usage.title')}
        </h2>
        <p class="my-4">{$_('privacy-policy.personal-data.usage.subtitle')}</p>
        <ul class="ml-8 list-disc">
          {#each getArrayFromLocale('privacy-policy.personal-data.usage.purposes') as x, i}
            <li>{$_(`privacy-policy.personal-data.usage.purposes.${i}`)}</li>
          {/each}
        </ul>
        <p class="my-4">
          {@html $_('privacy-policy.personal-data.usage.copy')}
        </p>

        {#each getArrayFromLocale('privacy-policy.personal-data.extra', $locale) as { title, copy }}
          <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
            {title}
          </h2>
          <p class="my-4">{copy}</p>
        {/each}

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.rights.title')}
        </h2>
        <p class="my-4">{$_('privacy-policy.rights.copy')}</p>
        <ol class="ml-8 list-decimal">
          {#each getArrayFromLocale('privacy-policy.rights.list', $locale) as { title, copy }}
            <li class="my-4">
              <h3 class="font-semibold text-l">{title}</h3>
              <p class="my-2">{copy}</p>
            </li>
          {/each}
        </ol>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.rights.exercise-rights.title')}
        </h2>
        <p class="my-4">
          {@html $_('privacy-policy.rights.exercise-rights.copy')}
        </p>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.additional-info.title')}
        </h2>
        <div class="mt-4">
          {#each getArrayFromLocale('privacy-policy.additional-info.infos', $locale) as item}
            <h3 class="font-semibold text-l">{item.title}</h3>
            {#each Array(Object.keys(item).length - 1) as x, i}
              <p class="my-4">{item[`copy.${i}`]}</p>
            {/each}
          {/each}
        </div>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.definitions.title')}
        </h2>
        <div class="mt-4">
          {#each definitions as { title, copy }}
            <h3 class="font-semibold text-l">{title}</h3>
            <p class="my-4">{copy}</p>
          {/each}
        </div>

        <h2 class="pt-4 text-xl font-semibold leading-6 tracking-wide">
          {$_('privacy-policy.change-warning.title')}
        </h2>
        <p class="my-4">{$_('privacy-policy.change-warning.copy')}</p>

      </div>
    </div>
  </div>
</section>
