<script>
  import Wave from "./decorational/Wave.svelte";
  import IconLink from "./IconLink.svelte"
</script>

<style>
  .bg-gradient {
    background: linear-gradient(180deg, #90cdf4, #3182ce);
  }

      .icon {
        height: 2rem;
        width: auto;
    }
</style>

<div class="relative">
  <div
    class="bg-gradient flex items-center justify-center pt-24 pb-16 w-full z-10">
    <div
      class="relative shadow-lg left-24 bg-gray-100 pt-4 pl-8 pr-32 rounded-lg
      max-w-3xl flex flex-col justify-center">
      <h1
        class="font-sans text-3xl font-bold text-gray-800 text-left mb-0
        antialiased">
        Hi, I am Rohan Faiyaz Khan
      </h1>
      <p class="self-end text-left text-lg text-gray-800 font-sans">
        I am a frontend engineer currently living in Dhaka, Bangladesh. I work
        with React, Javascript, Typescript and Svelte.
      </p>
      <div class="w-full h-10 mb-4 flex">
        <a href="mailto:rohankhan170@gmail.com" target="_blank" rel="noreferrer noopener">
          <img class="icon mr-4" src="social-icons/email.svg" alt="Rohan's email" />
        </a>
        <a href="https://github.com/rohanfaiyazkhan" target="_blank" rel="noreferrer noopener">
          <img class="icon mr-4" src="social-icons/github.svg" alt="Rohan's Github" />
        </a>
      </div>
    </div>
    <img
      class="relative shadow-lg block self-end rounded-full w-48 h-48 mr-0
      my-auto"
      src="me.jpg"
      alt="A picture of me" />
  </div>
  <Wave />
</div>
