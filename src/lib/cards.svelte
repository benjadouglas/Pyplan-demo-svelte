
<script>
	import { tweened } from 'svelte/motion';

	const _duration = 4000;

	const pr0 = tweened (0,{
		duration: _duration 
	})
	const pr1 = tweened (0,{
		duration: _duration
	})
	const pr2 = tweened (0,{
		duration: _duration
	})

	pr0.set(1);

	$: if ($pr0 === 1) {
		pr1.set(1)
	}

	$: if ($pr1 === 1) {
		pr2.set(1)
	}

	$: if ($pr2 === 1) {
        pr0.update(() => 0, { duration: 1 });
        pr1.update(() => 0, { duration: 1 });
        pr2.update(() => 0, { duration: 1 });
	}

    $: if ($pr0 === 0 && $pr1 === 0 && $pr2 === 0) {
        console.log("Restarting sequence");
        pr0.set(1);
    }
</script>

<div class="card-container">
	<div class="progress-container">
		<progress id="progress" value={$pr0} />
		<progress id="progress" value={$pr1} />
		<progress id="progress" value={$pr2} />
	</div>
	<div>
		{#if $pr0 <= 1 && $pr1 === 0}
			<div class="card" id="card-1">Plan</div>
		{:else if $pr1 <= 1 && $pr2 === 0}
			<div class="card" id="card-2">Discover</div>
		{:else if $pr1 === 1 && $pr2 >= 0}
			<div class="card" id="card-3">Execute</div>
		{/if}
	</div>
</div>

<style>

	.card-container {
		font-family: 'Poppins', sans-serif;
		font-size: 53.75px;
		font-weight: 900;
		justify-self: left;
		text-align: center;
		width: 50%;

		border-radius: 10px;
		--yellow: #f4dc59;
		background-color: var(--yellow);
	}

	.progress-container{
		padding: 0.5%;
		display: flex;
		flex-direction: row;
		flex-grow: inherit;
	}

	progress {
		flex: 1;
		width: 30%;
		height: 5px;
		opacity: 0.8;
		margin: 0.2% 0.5% 0 0.5%;
		border-radius: 8px;
		
		background: rgb(189, 189, 189);

		-webkit-appearance: none; 
		appearance: none;
	}

	progress::-webkit-progress-value {
		background-color: white;

		border-radius: 8px;
	}

	progress::-webkit-progress-bar {
		background-color: transparent;

		border-radius: 8px;
	}

	.card {
		height: 500px;
		display: flex;
		align-items: top;
		justify-content: left;
		font-size: 37.32px;
		margin: 0 0 0 1%;
		padding: 0;
	}


</style>
