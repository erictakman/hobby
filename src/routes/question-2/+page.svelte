<script>
	$: answer = '';
	
	$: correct = answer.toLowerCase() === 'and' ? true : false;
	
</script>

<div class="question-box">
	<h1>Vilket djur förknippas med platsen?</h1>
	<input type="text" bind:value={answer} />
	{#if (correct)}
		<p><b>Quak quak!</b> <br /> Måla Erics ringfinger</p>
		<aside style:background-color="#444cf7" />
		<a href="/question-3">Nästa</a>
	{:else}
		<img src="./images/q2img.jpg" alt="frågebild" />
		<img src="./images/q2.png" alt="kartbild" />
	{/if}
</div>
