<script>
	import '../styles/fonts.css';
</script>

<div class="question-box">
	<h1>Skattjakt!</h1>
	<a href="/question-1">Starta!</a>
</div>

<style>
	:global(*) {
		box-sizing: border-box;
	}

	:global(html) {
		font-family: 'Outfit', sans-serif;
		height: 100vh;
		width: 100vw;
		display: flex;
		justify-content: center;
		align-items: center;
		color: black;
		background-color: white;
		background-image: repeating-linear-gradient(
				45deg,
				#444cf7 25%,
				transparent 25%,
				transparent 75%,
				#444cf7 75%,
				#444cf7
			),
			repeating-linear-gradient(45deg, #fff44e 25%, #ff5526 25%, #ff5526 75%, #fff44e 75%, #fff44e);
		background-position: 0 0, 50px 50px;
		background-size: 100px 100px;
	}

	:global(body) {
		margin: 0;
	}

	:global(.question-box) {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		width: 90vw;
		padding: 1rem 0;
		gap: 1rem;
		background-color: white;
		border-radius: 1rem;
	}

	:global(input) {
		padding: 1rem;
		border-radius: 1rem;
		border: none;
		background-color: pink;
		color: black;
	}

	:global(h1) {
		font-size: x-large;
		padding: 0 2rem;
	}

	:global(h2) {
		font-size: large;
		padding: 0 1rem;
	}

	:global(a) {
		background-color: pink;
		padding: 0.8rem 1rem;
		border-radius: 1rem;
		text-decoration: none;
		color: black;
	}

	:global(aside) {
		width: 6rem;
		height: 8rem;
		border-radius: 6rem 6rem 4rem 4rem;
		border-bottom: 1rem solid pink;
		margin-bottom: 1rem;
	}

	:global(p) {
		font-size: large;
		line-height: 2rem;
		padding: 0 2rem;
	}

	:global(img) {
		width: 90%;
		object-fit: cover;
		border-radius: 1rem 1rem 1rem 1rem;
	}
</style>
