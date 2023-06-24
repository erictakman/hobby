<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'norra tullgränd' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vad heter gränden?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Snyggt!</b> <br /> Måla Erics lillfinger</p>
		<aside style:background-color="#ff5526" />
		<a href="/question-2">Nästa</a>
	{:else}
		<img src="./images/q1img.jpg" alt="frågebild" />
		<img src="./images/q1.png" alt="kartbild" />
	{/if}
</div>

