<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 's:t nikolai' ? true : false;
	
	$: showMap = false;
	$: image = showMap ? "q6.png" : "q6img.jpg";

</script>

<div class="question-box">
	<h1>Vem är förknippad med galleriet</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Fantastiskt, hoppas du har målat fint nu! 💅</b></p>
		<a href="/final">Nästa</a>
		{:else}
		<img on:click={() => showMap = !showMap} src="./images/{image}" alt="frågebild" />
	{/if}
</div>
