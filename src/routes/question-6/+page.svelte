<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 's:t nikolai' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vem är förknippad med galleriet</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Fantastiskt, hoppas du har målat fint nu! 💅</b></p>
		<a href="/final">Nästa</a>
	{:else}
		<img src="./images/q6img.jpg" alt="frågebild" />
		<img src="./images/q6.png" alt="kartbild" />
	{/if}
</div>
