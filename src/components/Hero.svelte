<script>
  import Wave from "./decorational/Wave.svelte";
</script>

<style>
  .bg-gradient {
    background: linear-gradient(180deg, #90cdf4, #3182ce);
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
    </div>
    <img
      class="relative shadow-lg block self-end rounded-full w-48 h-48 mr-0
      my-auto"
      src="me.jpg"
      alt="A picture of me" />
  </div>
  <Wave />
</div>
