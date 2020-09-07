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
  #container {
    position: relative;
    overflow: hidden;
    margin: 0 auto;
    width: 100%;
    max-width: 1140px;
  }
</style>

<div id="container">
  {#if $isLoading}
    <div class="loading">Loading...</div>
  {:else}
    <Header {segment} />

    <main>
      <slot />
    </main>

    <Footer {segment} />
  {/if}
</div>
