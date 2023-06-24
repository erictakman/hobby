<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'polhem' ? true : false;
	
	$: showMap = false;
	$: image = showMap ? "q3.png" : "q3img.jpg";

</script>

<div class="question-box">
	<h1>Vad heter den tekniska visionären?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Helt rätt!</b> <br /> Måla Erics långfinger</p>
		<aside style:background-color="#fff44e" />
		<a href="/question-4">Nästa</a>
		{:else}
		<img on:click={() => showMap = !showMap} src="./images/{image}" alt="frågebild" />
	{/if}
</div>

