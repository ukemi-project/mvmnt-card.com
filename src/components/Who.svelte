<script>
  import { _, locale, locales } from "svelte-i18n";

  export let segment;
</script>

<style>
  section {
    padding: 75px 0;
    padding-right: 0px;
    padding-left: 0px;
    display: block;
    background-color: var(--color-5);
  }

  .row {
    display: flex;
    justify-content: space-between;
    padding-left: 10%;
    padding-right: 10%;
    max-width: 1400px;
    margin: 0 auto;
  }

  .col-md-5 {
    position: relative;
    width: 100%;
    padding-right: 15px;
    padding-left: 15px;
  }
</style>

<section class="container-fluid black">
  <div class="row">
    <div class="col-md-5">
      <div class="subheading">In New York City</div>
      <div class="heading">
        Global Business
        <span class="br" />
        Enterprisess
      </div>
    </div>
    <div class="col-md-7">
      <div class="content">
        Curabitur mollis bibendum luctus. Duis suscipit vitae dui sed suscipit.
        Vestibulum auctor nunc vitae diam eleifend, in maximus metus
        sollicitudin. Quisque vitae sodales lectus. Nam porttitor justo sed mi
        finibus, vel tristique risus faucibus.
      </div>
      <div class="content">
        Curabitur mollis bibendum luctus. Duis suscipit vitae dui sed suscipit.
        Quisque vitae sodales lectus, vel tristique risus faucibus.
      </div>
    </div>
  </div>
</section>
<section class="pt-0 container-fluid black">
  <div class="row">
    <div class="col-md-4">
      <div class="col-feature">
        <div class="sub-color text-gradient">01.</div>
        <div class="heading">Website Design</div>
        <div class="content">
          Curabitur mollis bibendum luctus. Duis suscipit vitae dui sed
          suscipit. Vestibulum auctor nunc vitae lectus.
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="col-feature">
        <div class="sub-color text-gradient">02.</div>
        <div class="heading">Website Development</div>
        <div class="content">
          Curabitur mollis bibendum luctus. Duis suscipit vitae dui sed
          suscipit. Vestibulum auctor nunc vitae lectus.
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="col-feature">
        <div class="sub-color text-gradient">03.</div>
        <div class="heading">App Development</div>
        <div class="content">
          Curabitur mollis bibendum luctus. Duis suscipit vitae dui sed
          suscipit. Vestibulum auctor nunc vitae lectus.
        </div>
      </div>
    </div>
  </div>
</section>
