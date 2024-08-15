<script>
	import { Navbar, NavBrand, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<div class="relative px-8">
	<Navbar class="fixed start-0 top-0 w-full pt-6 pb-6 z-20" style="background-color:rgb(20,24,40);  box-shadow: 0 4px 20px -2px black;">
		<NavBrand href="/">
			<img src="info.png" class="me-3 h-6 sm:h-9" alt="About" />
			<span class="self-center whitespace-nowrap text-xl font-semibold text-white"
				>About this personal project</span
			>
		</NavBrand>
		<NavHamburger />
		<NavUl class="text-white">
			Thank you for visiting!
		</NavUl>
	</Navbar>
</div>

<style>

</style>