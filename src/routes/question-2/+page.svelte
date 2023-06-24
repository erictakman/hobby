<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'linnea' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter Erics syster?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p>Det är rätt! <br /> Måla Erics ringfinger</p>
		<aside style:background-color="#444cf7" />
		<a href="/question-3">Nästa</a>
	{/if}
</div>
