<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'kejsarträd' ? true : false;
	
	$: showMap = false;
	$: image = showMap ? "q4.png" : "q4img.jpg";

</script>

<div class="question-box">
	<h1>Vad är det för träd som står här?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Kungligt!</b> <br /> Måla Erics pekfinger</p>
		<aside style:background-color="#ff5526" />
		<a href="/question-5">Nästa</a>
		{:else}
		<img on:click={() => showMap = !showMap} src="./images/{image}" alt="frågebild" />
	{/if}
</div>
