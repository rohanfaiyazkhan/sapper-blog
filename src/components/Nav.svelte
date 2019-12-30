<script>
  export let segment;
</script>

<style>
  a {
    opacity: 0.7;
  }

  a.selected {
    opacity: 1;
  }

  a::before {
    content: "";
    position: absolute;
    transition: transform 0.3s ease;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 2px;
    background: #aaa;
    transform: scaleX(0);
  }

  a:hover::before,
  .selected::before {
    transform: scaleX(1);
  }

  .selected::before {
    background: #fd6378;
  }
</style>

<nav
  class="font-sans flex align-end justify-end flex-grow uppercase font-bold
  tracking-wide ">
  <a
    class={`no-underline text-gray-800 py-3 px-px sm:px-2 ml-2 text-md sm:text-lg md:text-xl relative ${segment === undefined ? 'selected' : ''}`}
    href="."
    rel="prefetch">
    blog
  </a>
  <a
    class={`no-underline text-gray-800 py-3 px-px sm:px-2 ml-2 text-md sm:text-lg md:text-xl relative ${segment === 'about' ? 'selected' : ''}`}
    href="about"
    rel="prefetch">
    about
  </a>
</nav>
