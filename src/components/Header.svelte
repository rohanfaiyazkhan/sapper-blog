<script>
  import Logo from "./Logo.svelte";
  import Nav from "./Nav.svelte";

  export let segment;
</script>

<style>
  .bg-gradient {
    background: linear-gradient(#bee3f8, #90cdf4);
  }
</style>

<div class="w-full bg-gradient">
  <header class="flex w-full mx-auto p-5 max-w-6xl items-center">
    <Logo />
    <Nav {segment} />
  </header>
</div>
