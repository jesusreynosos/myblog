<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	export let posts;
</script>

<style>
	  .Main-container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }
  .Main-content {
		margin: 0 0 1em 0;
		line-height: 1.5;
    display: grid;
    grid-template-columns: 3fr 1fr;
    grid-gap: 60px;
    justify-content: space-between;
  }
</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<div class="Main-container">
	<h1>Recent posts</h1>
	<div class="Main-content">	
	<ul>
	{#each posts as post}
		<li><a rel="prefetch" href="blog/{post.slug}">{post.title}</a></li>
	{/each}
</ul>
</div>
</div>