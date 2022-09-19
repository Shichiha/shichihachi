<script lang="ts">
	import DarkModeButton from './DarkModeButton.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
        let menuButton: HTMLButtonElement = document.querySelector("#menuButton")!
        menuButton.addEventListener("click", () => {
            let navItems: HTMLDivElement = document.querySelector("#navItems")!
            console.log(navItems)
            navItems.classList.toggle("hidden")
        })
    });
</script>

<div class="bg-slate-600 dark:bg-slate-800">
	<div class="flex flex-wrap items-center mx-auto p-4 md:p-8">
		<div class="flex items-center">
			<a href="/" class="flex text-white no-underline px-10">
				<span class="text-logo">shichihachi</span>
			</a>
		</div>
		
		
		<div class="nav-items hidden  md:block" id="navItems">
			<a href="/about">About</a>
			<a href="/contact">Contact</a>
			
		</div>
		<div class="ml-auto	">
			<div class="md:hidden inline-block">
		
				<button
				id="menuButton"
					class="navbar-burger flex items-center px-3 py-2 rounded text-white"
				>
					<svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"
						><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" /></svg
					>
				</button>
			</div>
			<DarkModeButton /> 
		</div>
	</div>
	
</div>


<!-- reposition this later -->
<style lang="scss" global>
	.navbar {
	@apply fixed text-white h-full float-left p-0 w-1/5 m-0 left-0 top-0 transition-all z-50;
	a {
		@apply no-underline block text-white p-4 indent-1 transition-all duration-200;
		@apply hover:bg-zinc-700 hover:indent-3 hover:text-white;
	}
}

.nav-items {
	@apply w-full flex-grow md:items-center md:w-auto md:flex-grow text-blue-200 text-lg;
	* {
		@apply block mt-4 md:inline-block md:mt-0 mr-6 no-underline font-medium hover:text-rose-50 text-center transition-all;
	}
}

.text-logo {
	@apply text-xl tracking-wide text-orange-600;
}
</style>