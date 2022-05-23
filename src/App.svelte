<script>
	//export let name;
	import Countdown from 'svelte-countdown/src/index.js';
	let isVisible = false;
	let jacketscenesrc = 'media/eren.png';
</script>

<main>
	<h1>The Abbenning Finishes In</h1>
	
	<Countdown from="2022-08-01 00:00:00" dateFormat="YYYY-MM-DD H:m:s" zone="America/New_York" let:remaining>
		<div class="timer">
			{#if remaining.done === false}
			<span>{remaining.years} years</span>
			<span>{remaining.months} months</span>
			<span>{remaining.weeks} weeks</span>
			<span>{remaining.days} days</span>
			<span>{remaining.hours} hours</span>
			<span>{remaining.minutes} minutes</span>
			<span>{remaining.seconds} seconds</span>
			{:else}
			<h2 style="font-weight: bold;">THE ABBENNING HAS CONCLUDED</h2>
			<p>🎉</p>
			{/if}
		</div>
	</Countdown>

	<img src={jacketscenesrc} alt="The Eren Yeager jacket scene from Attack on Titan">
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	img {
		padding: 25px;
	}

	span {
		font-weight: bold;
	}

</style>