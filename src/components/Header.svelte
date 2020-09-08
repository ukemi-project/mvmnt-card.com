<script>
  import Logo from "./Logo.svelte";
  import Nav from "./Nav.svelte";

  export let segment;
</script>

<style>
  header {
    /* position: fixed;
    width: 100%;
    height: 70px !important;
    padding-top: 10px;
    padding-bottom: 10px;
    background-color: var(--color-5);
    -webkit-transition: all 0.5s ease;
    -moz-transition: all 0.5s ease;
    -o-transition: all 0.5s ease;
    transition: all 0.5s ease;
    max-width: 1140px;
    z-index: 1; */

    padding: 10px 0;
    position: absolute;
    background-color: var(--color-5);
    -webkit-transition: all 0.5s ease;
    -moz-transition: all 0.5s ease;
    -o-transition: all 0.5s ease;
    transition: all 0.5s ease;
    top: 0;
    left: 0;
    width: 100%;
    height: auto;
    z-index: 999;

    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
  }

  .row {
    padding: 0 7%;
    max-width: 1400px;
    margin: 0 auto !important;
    width: 100%;
    justify-content: space-between;
    align-items: center;
  }
</style>

<header>
  <div>
    <div class="row">
      <Logo />
      <Nav {segment} />
    </div>
  </div>
</header>
