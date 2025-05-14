<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import Logo from '$lib/icons/logo.svelte';
	import Menu from '$lib/icons/menu.svelte';
	import Facebook from '$lib/icons/facebook.svelte';
	import Instagram from '$lib/icons/instagram.svelte';
	import Twitter from '$lib/icons/twitter.svelte';

  let isOpen = $state(false);
  const toggleMenu = () => isOpen = !isOpen;
</script>

<nav class="fixed top-0 z-50 h-20 w-full bg-[#141415] md:px-20 lg:px-[150px] pt-2">
	<!-- <div class="flex justify-between"> -->
  <div class="w-full 2xl:flex h-16 items-center lg:justify-between gap-5">
    <div class="flex items-center justify-between gap-8 px-4 py-2">
      <Logo data="w-40 h-10" />

      <ul class="hidden 2xl:flex gap-5 text-white">
        <li class="text-lg font-medium">About</li>
        <li class="text-lg font-medium">Solutions</li>
        <li class="text-lg font-medium">Insights</li>
        <li class="text-lg font-medium">Contact</li>
      </ul>

      <button class="2xl:hidden" onclick={toggleMenu} aria-label="Toggle menu">
        <Menu data="w-8 h-8 fill-[#ffffff]" />
      </button>
    </div>

    <div class="hidden 2xl:flex items-center gap-5">
      <button class="h-12 w-36 rounded-xl bg-gray-700 text-lg font-medium text-white">
        We're hiring
      </button>
      <button class="h-12 w-36 rounded-xl bg-blue-700 text-lg font-medium text-white">
        Contact Sales
      </button>
    </div>
  </div>

  {#if isOpen}
    <ul class="flex flex-col w-full gap-5 bg-[#141415] p-5 text-white 2xl:hidden mt-2">
      <li class="text-lg font-medium">About</li>
      <li class="text-lg font-medium">Solutions</li>
      <li class="text-lg font-medium">Insights</li>
      <li class="text-lg font-medium">Contact</li>
    </ul>
  {/if}
<!-- </div> -->
</nav>

{@render children()}

<footer class="bg-[#141415] px-6 py-12 text-white lg:px-16">
	<div class="flex flex-col lg:flex-row justify-between gap-8 md:gap-0 px-0 lg:px-32">
		<div class="w-full md:w-96 space-y-4">
			<div class="flex items-start md:items-center">
				<Logo data="w-52 h-16" />
			</div>
			<p class="text-lg leading-relaxed text-gray-400">
				Our beautiful designs open the door to a realm of limitless possibilities, where imagination
				knows no bounds.
			</p>
		</div>

		<div>
			<h3 class="mb-4 text-xl font-semibold text-white">Company</h3>
			<ul class="space-y-3 text-base text-gray-400">
				<li><a href="/">About</a></li>
				<li><a href="/">Solutions</a></li>
				<li><a href="/">Insights</a></li>
				<li><a href="/">Contact</a></li>
			</ul>
		</div>

		<div>
			<h3 class="mb-4 text-xl font-semibold text-white">Company</h3>
			<ul class="space-y-3 text-base text-gray-400">
				<li><a href="/">About</a></li>
				<li><a href="/">Solutions</a></li>
				<li><a href="/">Insights</a></li>
				<li><a href="/">Contact</a></li>
			</ul>
		</div>

		<div>
			<h3 class="mb-4 text-xl font-semibold text-white">Get in touch</h3>
			<p class="mb-4 text-base text-gray-400">hello@company.com</p>
			<div class="flex space-x-4">
				<a href="/" class=" bg-gray-800 p-2 hover:bg-gray-700"><Facebook /></a>
				<a href="/" class=" bg-gray-800 p-2 hover:bg-gray-700"><Twitter /></a>
				<a href="/" class=" bg-gray-800 p-2 hover:bg-gray-700"><Instagram /></a>
			</div>
		</div>
	</div>

	<div
		class="mt-10 flex flex-col items-center justify-between border-t border-gray-700 
		md:px-32 pt-6 text-sm text-gray-500 md:flex-row"
	>
		<p>© Sierra WordPress Theme. All Rights Reserved.</p>
		<div class="mt-4 flex space-x-6 md:mt-0">
			<a href="/" class="hover:text-white">Terms & Conditions</a>
			<a href="/" class="hover:text-white">Privacy Policy</a>
		</div>
	</div>
</footer>
