<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'mormor' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter Erics mormor?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p>Det är rätt! <br /> Måla Erics tumme</p>
		<aside style:background-color="#fff44e" />
		<a href="/question-6">Nästa</a>
	{:else}
		<p>Det är fel!</p>
	{/if}
</div>
