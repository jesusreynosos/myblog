<script>
	let darkMode = false;
	function toggle() {
        darkMode = !darkMode;
        window.document.body.classList.toggle('dark');
    }
</script>

<button on:click={toggle}>
	{#if darkMode }
		🌞
	{:else}
		🌙
	{/if}
</button>

<style>
	button {
		background: #6a6a6a;
		border: 2px solid var(--text-color);
		border-radius: 5px;
		color: inherit;
    padding: 10px 15px;
    display: inline-block;
    
	}
	
	button:active {
		background: #aeaeae;
	}
</style>