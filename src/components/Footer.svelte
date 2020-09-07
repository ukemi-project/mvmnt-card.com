<script>
  import { _, locale, locales } from "svelte-i18n";
  export let segment;
</script>

<style>
  footer {
    width: 100%;
    background-color: var(--color-5);
    z-index: 100;
    padding: 10px 0 5px 0;
  }

  .footer_box {
    width: 90%;
    max-width: 1140px;
    margin: 0 auto;
    padding-left: 5%;
    padding-right: 5%;
  }

  .copyright {
    width: 100%;
    text-align: center;
    padding-top: 15px;
  }

  .copyright p {
    color: var(--color-3) !important;
    font-size: 15px;
  }
</style>

<footer class="top_border">
  <div class="footer_box">
    <div class="row">
      <div class="twelvecol up_fade">
        <div class="copyright ">
          <p>
            Copyright © 2019
            <a href="https://ukemi.ninja">Ukemi</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</footer>
