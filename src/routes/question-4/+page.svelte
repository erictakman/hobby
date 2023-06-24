<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'kejsarträd' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad är det för träd som står här?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Kungligt!</b> <br /> Måla Erics pekfinger</p>
		<aside style:background-color="#ff5526" />
		<a href="/question-5">Nästa</a>
	{:else}
		<img src="./images/q4img.jpg" alt="frågebild" />
		<img src="./images/q4.png" alt="kartbild" />
	{/if}
</div>
