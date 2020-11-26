<svelte:head>
	<title>Blog de educación en medicina: Contacto</title>
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

<script>
  import analyticsTracking from '../utils/analytics';
</script>

<div class="Contact">
  <h2>Contact me</h2>
	<p>You can find me at:  </p>
	<a href="https://www.twitter.com/jdemiliano" target="_blank" rel="noreferrer" on:click={analyticsTracking('twitter')}>
	<p>Twitter </p></a>
	<a href="https://www.linkedin.com/in/jesusdavidemiliano" target="_blank" rel="noreferrer" on:click={analyticsTracking('linkedin')}>
	<p>LinkedIn </p></a>
	<a href="https://mailto:rjsd13@gmail.com" target="_blank" rel="noreferrer" on:click={analyticsTracking('mail')}>
  <p>Email (recomendado) </p></a>
</div>