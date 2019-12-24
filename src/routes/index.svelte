<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`post.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      });
  }
</script>

<script>
  export let posts;
</script>

<style>
  .home-container {
    align-items: center;
    display: flex;
    flex-direction: column;
    flex: 1;
    justify-content: center;
    margin: 2em 0;
    min-height: 400px;
  }

  .home-copy {
    flex: 1;
  }

  h1 {
    font-weight: 700;
    margin-bottom: 0.5em;
  }

  p {
    font-size: 1.4em;
    line-height: 1.5;
  }

  .blog-container {
    max-width: 780px;
    margin: 60px auto;
  }

  h2,
  .post-item-footer {
    font-family: Rubik, sans-serif;
    font-weight: 700;
  }

  .post-item-date {
    color: #aaa;
    text-align: left;
    text-transform: uppercase;
    margin-right: 16px;
  }

  hr {
    margin: 60px auto;
  }

  @media (max-width: 1020px) {
    p {
      font-size: 1.2em;
    }
  }

  @media (max-width: 800px) {
    .home-container {
      flex-direction: column;
    }

    .home-copy {
      flex: 0;
      padding-bottom: 2em;
      text-align: center;
    }
  }
</style>

<svelte:head>
  <title>Sapper Blog Template</title>
</svelte:head>

<div class="home-container">
  <div class="home-copy">
    <h1>Welcome to your new Sapper Blog</h1>
    <p>
      Check out the docs on
      <a
        href="https://www.github.com/Charca/sapper-blog-template"
        target="_blank">
        GitHub
      </a>
      to get started.
    </p>
  </div>

  <div class="blog-container">
    <h1>Blog</h1>
    {#each posts as post, index}
      {#if index}
        <hr />
      {/if}
      <div class="post-item">
        <h2>
          <a rel="prefetch" href="post/{post.slug}">{post.title}</a>
        </h2>
        <p>{post.excerpt}</p>
        <div class="post-item-footer">
          <span class="post-item-date">— {post.printDate}</span>
        </div>
      </div>
    {/each}
  </div>

</div>
