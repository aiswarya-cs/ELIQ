<script lang="ts">
	interface product {
		heading: string;
		paragraph: string;
	}

	const ProductData: product[] = [
		{
			heading: 'Products',
			paragraph:
				'Dive into the future of next-generation technology with our business custom tailored software.'
		},
		{
			heading: 'Products',
			paragraph:
				'Dive into the future of next-generation technology with our business custom tailored software.'
		},
		{
			heading: 'Products',
			paragraph:
				'Dive into the future of next-generation technology with our business custom tailored software.'
		}
	];
</script>

<div class="mt-10 grid grid-cols-1 gap-6 sm:grid-cols-1 lg:grid-cols-3">
	{#each ProductData as items}
		<div class="flex w-full flex-col gap-4 rounded-xl bg-[#1d1f20] p-8 text-white">
			<h3 class="text-2xl font-semibold">{items.heading}</h3>
			<p class="text-gray-400">{items.paragraph}</p>
			<button
				class="h-12 w-48 rounded-xl bg-blue-700 text-base font-medium hover:border hover:border-blue-700 hover:bg-white hover:text-blue-700"
			>
				View products
			</button>
		</div>
	{/each}
</div>
