<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'pappa' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter Erics pappa?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p>Det är rätt! <br /> Måla Erics långfinger</p>
		<aside style:background-color="#fff44e" />
		<a href="/question-4">Nästa</a>
	{/if}
</div>

