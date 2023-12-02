<script>
	import Cards from '$lib/main/cards.svelte';
	import Title from '$lib/main/title.svelte';
	import NavBar from '$lib/main/navBar.svelte';
</script>

<div class="nav-bar">
	<NavBar></NavBar>
</div>
<div class="top">
	<Title></Title>
	<Cards></Cards>
</div>

<style>
	.nav-bar {
		position: absolute;
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 2fr 1fr;
		/* align-items: center; */
		justify-items: center;
	}

	.top {
		position: relative;
		margin: 60px 10px 0 10px;
		display: grid;

		grid-template-columns: 1fr 1fr;
		gap: 20px;
		align-items: center;
	}
</style>
