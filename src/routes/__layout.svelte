<script>
	import css from '../styles/global.css';
</script>

<main>
	<header>
		<p class="subtitle">Made with Svelte</p>
		<h1 class="title">Shichihachi's page</h1>
	</header>
	<div class="content">
		<slot />
	</div>
	<footer>
		<p>manducare dolorem tuum sicut subcinericius.</p>
	</footer>
</main>

<style>
	footer {
		position: absolute;
		bottom: 0;
		width: 100%;
		height: 5%;
		background-color: #00000053;
	}
	header {
		position: absolute;
		top: 0;
		width: 100%;
		height: 50px;
		background-color: #00000053;
		padding: 0;
		margin: 0;
	}
	p,
	h1 {
		padding-left: 10px;
	}
	.title,
	.subtitle {
		position: absolute;
		right: 1%;
	}
	.subtitle {
		color: #ffffff8d;
	}
	.content {
		position: absolute;
		top: 50px;
		bottom: 50px;
		left: 0;
		right: 0;
		display: flex;
		flex-direction: column;
        justify-content: center;
        align-items: center;
	}
	p {
		margin: 5px;
		font-size: large;
	}
</style>
