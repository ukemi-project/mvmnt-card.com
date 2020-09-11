<script>
  import Logo from "./Logo.svelte";
  import Nav from "./Nav.svelte";

  export let segment;
</script>

<div class="relative shadow bg-mcblack">
  <header class="px-4 mx-auto max-w-7xl sm:px-10">
    <div
      class="flex items-center justify-between py-2 md:justify-start md:space-x-10">
      <Logo />
      <Nav {segment} />
    </div>
  </header>
</div>
