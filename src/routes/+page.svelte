<script>
	import Cards from '$lib/main/cards.svelte';
	import Title from '$lib/main/title.svelte';
	import NavBar from '$lib/main/navBar.svelte';
</script>

<div class="main-body">
	<div class="nav-bar">
		<NavBar></NavBar>
	</div>
	<div class="top">
		<Title></Title>
		<Cards></Cards>
	</div>
</div>

<style>
	.main-body {
		height: 90vh;
		background: var(--bg-color-primary);
		background-image: linear-gradient(to bottom, var(--bg-color-primary), transparent),
			linear-gradient(to top, var(--bg-color-primary), transparent),
			radial-gradient(black 1px, transparent 0);
		background-size:
			100% 100%,
			100% 10%,
			15px 15px;
		background-repeat: no-repeat, no-repeat, repeat;
		background-position:
			top,
			bottom,
			0 0;
	}
	.nav-bar {
		position: absolute;
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 2fr 1fr;
		align-items: center;
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
