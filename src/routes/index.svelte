<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	import Post from '../components/Post.svelte'
	export let posts;
</script>

<style>
	.Posts {
		display:grid;
		justify-content: space-between;
		grid-gap: 15px;
		grid-template-columns: 1fr;
	}
</style>

<svelte:head>
	<title>Current trends in health</title>
	<meta name="description" content="Blog de Jesus Reynoso" />
	
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:side" content="@jesusreynoso_"/>
	<meta name="twitter:creator" content="@jesusreynoso_" />
	<meta name="twitter:title" content="FuturoMedico" />
	<meta name="twitter:description" content="Blog de Innovación en Medicina" />
	<meta name="twitter:image" content="https://futuromdrss.s3-us-west-1.amazonaws.com/RSS1Mesa+de+trabajo+1%402x.png" />

	<meta name="og:title" content="FuturoMedico" />
	<meta name="og:description" content="Blog de Innovación en Medicina" />
	<meta name="og:image" content="https://futuromdrss.s3-us-west-1.amazonaws.com/RSS1Mesa+de+trabajo+1%402x.png" />
	<meta name="og:url" content="https://futuromedi.co" />
	<meta name="og:site_name" content="FuturoMedico" />
	<meta name="og:locale" content="es_ES" />
	<meta name="og:type" content="article" />
	<meta name="fb:app_id" content="681944209173500" />

</svelte:head>

<div class="Home">
	<div class="Posts">
		{#each posts as post}
			<Post {post} />
		{/each}
	</div>
</div>