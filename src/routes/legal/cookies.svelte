<script>
  import { _, locale } from "svelte-i18n";
  import getArrayFromLocale from "../../utils/getArrayFromLocale";
  $: content = getArrayFromLocale("cookies.content", $locale);
</script>

<svelte:head>
  <title>{$_('cookies.title')} | Welcome To My Garden</title>
</svelte:head>

<h1>{$_('cookies.title')}</h1>
{#each content as { title, html }}
  <h2 class="title">{title}</h2>
  <p>
    {@html html}
  </p>
{/each}
