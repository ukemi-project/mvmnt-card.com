<script>
  import { _, locale, locales } from "svelte-i18n";
  export let segment;
</script>

<style>
  footer {
    z-index: 100;
    background-color: var(--color-5);
    width: 100%;
    margin-top: 90px;
    padding: 20px 15px;
  }

  .row {
    display: flex;
    padding-left: 10%;
    padding-right: 10%;
    max-width: 1500px;
    margin: 0 auto;
    max-width: 1400px;
  }
  .copyright {
    text-align: center;
    font-size: 0.8rem;
    opacity: 1;
    letter-spacing: 0.1em;
    margin: 0;
    color: #eee;
  }

  a {
    color: var(--color-orange);
    font-size: 1rem;
  }
</style>

<footer>
  <div class="row">
    <div class="twelvecol up_fade">
      <div class="copyright ">
        © Copyright 2020
        <a href="https://ukemi.ninja">Ukemi</a>
        {$_('copywrite')}
      </div>
    </div>
  </div>
</footer>
