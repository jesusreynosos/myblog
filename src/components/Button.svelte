<script>
function toggle() {
  window.document.body.classList.toggle('dark-mode')
  window.document.header.classList.toggle('dark-mode')
}
</script>
<button on:click={toggle}>
	<slot/>
</button>
<style>
	button {
		background-color: #f76027;
		color: white;
		border: none;
		border-radius: 4px;
		padding: 0.5rem;
	}
</style>