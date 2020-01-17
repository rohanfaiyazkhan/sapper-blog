<style>
  .wave {
    display: block;
    z-index: 0;
    width: 100%;
    height: 300px;
    object-fit: cover;
    position: absolute;
    left: 0;
    top: 100%;
  }

  @media (max-width: 640px) {
    .wave {
      display: none;
    }
  }
</style>

<img class="wave z-0" src="wave.svg" alt="" />
