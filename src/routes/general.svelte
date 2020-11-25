<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
  import Post from '../components/Post.svelte';
  export let posts;
  const filterPost = posts.filter(({primary_tag}) => primary_tag && primary_tag.name === 'Machine Learning' || 'Getting Started')
</script>

<style>
  .Posts {
    display:grid;
    justify-content: space-between;
    grid-gap: 30px;
    grid-template-columns: 1fr;
  }
</style>

<svelte:head>
	<title>Blog de educación en medicina: General</title>
	<meta name="description" content="Blog de Jesus Reynoso" />
	
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:side" content="@jdemiliano"/>
	<meta name="twitter:creator" content="@jdemiliano" />
	<meta name="twitter:title" content="FuturoMedico" />
	<meta name="twitter:description" content="Blog de Educacion en Medicina" />
	<meta name="twitter:image" content="https://arepa.s3.amazonaws.com/blogpost-cover.png" />

	<meta name="og:title" content="FuturoMedico" />
	<meta name="og:description" content="Blog de Educacion en Medicina" />
	<meta name="og:image" content="https://arepa.s3.amazonaws.com/blogpost-cover.png" />
	<meta name="og:url" content="https://futuromedi.co/about" />
	<meta name="og:site_name" content="FuturoMedico" />
	<meta name="og:locale" content="es_ES" />
	<meta name="og:type" content="article" />
	<meta name="fb:app_id" content="681944209173500" />

</svelte:head>

<div class="General">
  <h1>General</h1>
  <div class="Posts">
    {#if filterPost.length >= 1}
      {#each filterPost as post}
        <Post {post} />
      {/each}
    {:else}
      <p>Sin resultados...</p>
    {/if}
  </div>
</div>