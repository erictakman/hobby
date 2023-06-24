<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'polhem' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter den tekniska visionären?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Helt rätt!</b> <br /> Måla Erics långfinger</p>
		<aside style:background-color="#fff44e" />
		<a href="/question-4">Nästa</a>
	{:else}
		<img src="./images/q3img.jpg" alt="frågebild" />
		<img src="./images/q3.png" alt="kartbild" />
	{/if}
</div>

