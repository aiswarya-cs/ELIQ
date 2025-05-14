<script lang="ts">
	import BgLines from "$lib/icons/bg-lines.svelte";

</script>
<div
			class="relative flex w-full flex-col items-center justify-center overflow-hidden rounded-lg"
		>
			<BgLines
				data="absolute bg-blue-600 bg-contain bg-center bg-repeat rounded-lg w-full lg:w-4/5 py-20 h-auto"
			/>
<div class="relative z-10 flex flex-col items-center justify-center px-4 py-20 text-center">
	<h1 class="mb-4 text-3xl font-bold text-white md:text-5xl">Transform Your Business Today!</h1>
	<p class="max-w-2xl text-lg text-white md:text-xl">
		Join hands with Web Eliq and take your business to the next level. Whether you need a custom
		software solution, cloud migration, or a strong digital presence, we are here to help.
	</p>

	<div class="mt-5 flex-col gap-2 md:mt-8 md:flex-row">
		<input
			type="email"
			placeholder="Email"
			class="w-96 rounded-md px-4 py-2 text-black outline-none md:w-auto"
		/>
		<button class="mt-5 w-52 rounded-md bg-black px-4 py-2 text-white md:mt-0 md:w-auto">
			Let’s Innovate Together!
		</button>
	</div>
</div>
</div>
