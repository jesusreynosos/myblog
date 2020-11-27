<script>
	function toggle() {
	window.document.body.classList.toggle('dark-mode');
}
</script>

<div class="Button">
<button on:click={toggle}>
	<slot/>
</button>
</div>

<style>
	button {
		background-color: #f76027;
		color: white;
		border: none;
		border-radius: 4px;
		padding: 0.5rem;
	}
</style>