<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'petrus' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vilken De Dacia är ingraverad på stentavlan?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Mycket bra, snart där!</b> <br /> Måla Erics tumme</p>
		<aside style:background-color="#fff44e" />
		<a href="/question-6">Nästa</a>
	{:else}
		<img src="./images/q5img.jpg" alt="frågebild" />
		<img src="./images/q5.png" alt="kartbild" />
	{/if}
</div>
