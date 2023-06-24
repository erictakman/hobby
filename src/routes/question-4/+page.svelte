<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'mamma' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter Erics mamma?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p>Det är rätt! <br /> Måla Erics pekfinger</p>
		<aside style:background-color="#ff5526" />
		<a href="/question-5">Nästa</a>
	{/if}
</div>
