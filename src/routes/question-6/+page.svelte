<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'rolf' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter Erics Rolf?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p>Det är rätt!</p>
		<a href="/final">Nästa</a>
	{/if}
</div>
