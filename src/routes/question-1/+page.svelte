<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'norra tullgränd' ? true : false;

	$: showMap = false;
	$: image = showMap ? "q1.png" : "q1img.jpg";
	
</script>

<div class="question-box">
	<h1>Vad heter gränden?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Snyggt!</b> <br /> Måla Erics lillfinger</p>
		<aside style:background-color="#ff5526" />
		<a href="/question-2">Nästa</a>
	{:else}
		<img on:click={() => showMap = !showMap} src="./images/{image}" alt="frågebild" />
	{/if}
</div>

