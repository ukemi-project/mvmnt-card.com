<script>
  import Logo from "./Logo.svelte";
  import Nav from "./Nav.svelte";

  export let segment;
</script>

<style>
  header {
    position: fixed;
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
    z-index: 1;
  }

  .header {
    width: 90%;
    max-width: 1140px;
    margin: 0 auto;
    padding-left: 5%;
    padding-right: 5%;
  }
</style>

<header>
  <div class="header">
    <Logo />
    <Nav {segment} />
  </div>
</header>
