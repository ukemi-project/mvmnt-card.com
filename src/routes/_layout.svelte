<script context="module">
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

<style>
  .wrapper {
    padding: 0;
    display: block;
  }
</style>

{#if $isLoading}
  <div class="loading">Loading...</div>
{:else}
  <div class="wrapper">
    <!-- <Header {segment} /> -->

    <main>
      <slot />
    </main>

    <!-- <Footer {segment} /> -->
  </div>
{/if}
