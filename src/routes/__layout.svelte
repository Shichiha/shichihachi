<script>
	import Navbar from './../lib/Navbar.svelte';
	import '../styles/global.scss';
</script>

<Navbar />

<slot />

<style>
	#avatar {
		border-radius: 50%;
		margin-bottom: 20px;
		width: 50%;
		transition: 1s;
	}
	#avatar:hover {
		transform: scale(1.1);
	}
</style>
