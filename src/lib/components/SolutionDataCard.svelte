<script lang="ts">
	interface solution {
		image: string;
		head: string;
		description: string;
		buttonText: string;
	}

	const solutionData: solution[] = [
		{
			image: 'images/saas-icon-3.png',
			head: 'Scalability optimization',
			description:
				'Our scalability solutions analyze your current infrastructure, identifying bottlenecks and optimizing processes.',
			buttonText: 'Learn More'
		},
		{
			image: 'images/saas-icon-9.png',
			head: 'Scalability optimization',
			description: 'Our scalability solutions analyze your current infrastructure.',
			buttonText: 'Learn More'
		},
		{
			image: 'images/saas-icon-3.png',
			head: 'Scalability optimization',
			description:
				'Our scalability solutions analyze your current infrastructure, identifying bottlenecks and optimizing processes.',
			buttonText: 'Learn More'
		},
		{
			image: 'images/saas-icon-9.png',
			head: 'Scalability optimization',
			description:
				'Our scalability solutions analyze your current infrastructure, identifying bottlenecks and optimizing processes.',
			buttonText: 'Learn More'
		},
		{
			image: 'images/saas-icon-3.png',
			head: 'Scalability optimization',
			description:
				'Our scalability solutions analyze your current infrastructure, identifying bottlenecks and optimizing processes.',
			buttonText: 'Learn More'
		},
		{
			image: 'images/saas-icon-9.png',
			head: 'Scalability optimization',
			description:
				'Our scalability solutions analyze your current infrastructure, identifying bottlenecks and optimizing processes.',
			buttonText: 'Learn More'
		}
	];
</script>

<div class="w-full px-4 py-8 sm:px-6 md:px-10 lg:px-20">
	<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 2xl:grid-cols-3">
		{#each solutionData as items}
			<div class="flex h-full min-h-[320px] w-full flex-col rounded-lg bg-white p-6 text-black">
				<img src={items.image} alt="" class="h-8 w-8" />
				<div class="mt-5 flex flex-grow flex-col justify-between">
					<div class="flex flex-col gap-4">
						<h1 class="text-xl font-semibold sm:text-2xl">{items.head}</h1>
						<p class="text-[15px] text-[#5b5b5c] sm:text-[17px]">{items.description}</p>
					</div>
					<button
						class="mt-5 h-10 w-full rounded-lg bg-[#fafafc] p-2 text-base font-medium text-blue-700 sm:w-40"
					>
						{items.buttonText}
					</button>
				</div>
			</div>
		{/each}
	</div>
</div>
