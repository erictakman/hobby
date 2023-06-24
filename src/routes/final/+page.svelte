<script>
	import Confetti from './Confetti.svelte'

	$: correct = false;
	$: currentNail = 1;
	$: colors = ["#f3a8b1", "#f3a8b1", "#f3a8b1", "#f3a8b1", "#f3a8b1"]

	const setColor = (color) => {
		if (currentNail === 1) {
			colors[0] = color
			currentNail++;
		} else if (currentNail === 2) {
			colors[1] = color
			currentNail++;
		} else if (currentNail === 3) {
			colors[2] = color
			currentNail++;
		} else if (currentNail === 4) {
			colors[3] = color
			currentNail++;
		} else if (currentNail === 5) {
			colors[4] = color
			if (
				colors[0] === '#ff5526' &&
    		colors[1] === '#444cf7' &&
    		colors[2] === '#fff44e' &&
    		colors[3] === '#ff5526' &&
    		colors[4] === '#fff44e'
			) {
				setTimeout(() => {
					console.log("correct")
					correct = true;
				}, 500)
			} else {
				setTimeout(() => {
					correct = false;
					colors = ["#f3a8b1", "#f3a8b1", "#f3a8b1", "#f3a8b1", "#f3a8b1"]
					currentNail = 1;
				}, 500)
			}
		}
	}

</script>

<div class="question-box">
	<h1>Vilka färger har Eric på naglarna?</h1>
	<div class="nails">
		{#each colors as color}
			<div class="nail" style:background-color={color} />
		{/each}
	</div>
	<div class="answers">
		<div class="orange" on:click={() => setColor("#ff5526")} />
		<div class="yellow" on:click={() => setColor("#fff44e")}/>
		<div class="blue" on:click={() => setColor("#444cf7")}/>
	</div>
	{#if correct}
		<section>
			<div class="container">
				<Confetti durationInSeconds={2} />
			</div>
			<a href="https://rettodsmot.se/">rettodsmot.se</a>
		</section>
	{/if}
</div>

<style>
	.nails {
		display: flex;
		justify-content: space-evenly;
		width: 300px;
		margin-bottom: 2rem;
	}

	.nail {
		height: 65px;
		width: 45px;
		border-radius: 2rem 2rem 1rem 1rem;
		border-bottom: 0.4rem solid pink;
	}

	.answers {
		display: flex;
		justify-content: space-between;
		width: 300px;
		margin: 0 auto;
		margin-bottom: 1rem;
	}
	
	.orange {
		background-color: #ff5526;
		height: 75px;
		width: 75px;
		border-radius: 25%;
		border: 0.4rem solid pink;
		margin: 0 auto;
	}

	.yellow {
		background-color: #fff44e;
		height: 75px;
		width: 75px;
		border-radius: 25%;
		border: 0.4rem solid pink;
		margin: 0 auto;
	}

	.blue {
		background-color: #444cf7;
		height: 75px;
		width: 75px;
		border-radius: 25%;
		border: 0.4rem solid pink;
		margin: 0 auto;
	}

	.container {
		width: 500px;
		margin: 0 auto;
		top: 50%;
		left: 50%;
		position: fixed;
	}

	section {
		position: relative;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		width: 100vw;
		background-color: white;
		position: absolute;
	}
</style>
