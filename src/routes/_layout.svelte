<script context="module">
  import Tailwindcss from "../Tailwindcss.svelte";
  import { isLoading, waitLocale } from "svelte-i18n";
  export async function preload(page) {
    return waitLocale();
  }
</script>

<script>
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";

  export let segment;
</script>

<Tailwindcss />
{#if $isLoading}
  <div class="loading">Loading...</div>
{:else}
  <div class="relative flex flex-col h-screen">

    <Header {segment} />

    <main class="inset-0 flex-grow">
      <slot />
    </main>

    <Footer {segment} />
  </div>
{/if}
