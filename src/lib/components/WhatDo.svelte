<script lang="ts">
	interface whatdo {
		text: string;
		colored: string;
		paragraph: string;
	}

	const whatDo: whatdo[] = [
		{
			text: 'Innovation-Driven ',
			colored: 'Solutions',
			paragraph: 'We leverage the latest technologies to craft future-ready solutions'
		},
		{
			text: 'End-to-End',
			colored: 'Support',
			paragraph: 'From strategy to execution, we ensure seamless implementation and maintenance'
		},
		{
			text: 'Tailored',
			colored: 'Approach',
			paragraph: 'Every solution is customized to fit your business requirements.'
		},
		{
			text: 'Client-Centric',
			colored: 'Focus',
			paragraph: 'Your success is our priority; we collaborate closely to achieve your goals.'
		}
	];
</script>

<div class="flex items-center justify-center py-5 md:py-20">
	<div class="mx-5 grid grid-cols-1 gap-5 md:grid-cols-1 lg:grid-cols-4">
		{#each whatDo as item}
			<div class="flex w-full flex-col gap-5 rounded-lg bg-[#1d1f20] p-5 md:p-14 lg:w-72">
				<h1 class="text-2xl font-medium">
					{item.text} <br class="hidden md:flex" />
					<span class="text-blue-700">{item.colored}</span>
				</h1>
				<p class="font-medium text-[#737474]">{item.paragraph}</p>
			</div>
		{/each}
	</div>
</div>
