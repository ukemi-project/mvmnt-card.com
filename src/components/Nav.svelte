<script>
  import { _, locale, locales } from "svelte-i18n";
  export let segment;
</script>

<style>
  nav {
    margin: 0;
    float: right;
    position: relative;
  }

  li {
    display: inline-block;
    position: relative;
    margin: 24px 12px 0 12px;
  }

  li :last-child {
    margin-right: 0;
  }

  a {
    display: inline-block;
    text-align: center;
    padding: 0;
    font-size: 20px;
    line-height: 18px;
    font-weight: 100;
    font-family: var(--font-heading);
    color: var(--color-1);
  }

  a:hover {
    color: var(--color-orange);
  }

  a:not(.selected) {
    opacity: 0.7;
  }
</style>

<nav class={$_('direction')} role="navigation">
  <ul class={$_('direction')}>
    <li>
      <a class:selected={segment === undefined} href=".">{$_('nav.home')}</a>
    </li>
    <li>
      <a class:selected={segment === 'about'} href="about">{$_('nav.about')}</a>
    </li>
    <li>
      <a rel="prefetch" class:selected={segment === 'blog'} href="blog">
        {$_('nav.blog')}
      </a>
    </li>
    {#each $locales as item}
      <li>
        <span
          class="a"
          class:selected={$locale.includes(item)}
          href={`#!${item}`}
          on:click={() => ($locale = item)}>
          {$_('languages.' + item.replace('-', '_'))}
        </span>
      </li>
    {/each}
  </ul>
</nav>
