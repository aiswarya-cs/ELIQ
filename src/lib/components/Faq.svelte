<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';

	interface faq {
		question: string;
		answer: string;
	}

	const faqData: faq[] = [
		{
			question: 'What industries do you serve?',
			answer: `We work with businesses across various industries, including healthcare, 
				finance, retail, education, and more, providing tailored technology solutions.`
		},
		{
			question: 'Do you offer custom software development?',
			answer: `Yes, we specialize in developing custom software solutions designed to meet the
				 specific needs of your business.`
		},
		{
			question: 'What cloud platforms do you support?',
			answer: `We provide cloud infrastructure setup and management on AWS, Azure, GCP,
			 and Digital Ocean.`
		},
		{
			question: 'Do you provide ongoing support and maintenance?',
			answer: `Yes, we offer end-to-end support, including maintenance and upgrades to
			 ensure your IT systems remain secure and up to date.`
		},
		{
			question: 'How can Web Eliq help improve my online presence?',
			answer: `Our digital services include website development, SEO, social media 
			marketing, and branding to enhance your visibility and engagement online.`
		},
		{
			question: 'What industries do you serve?',
			answer: `We work with businesses across various industries, including healthcare, 
				finance, retail, education, and more, providing tailored technology solutions.`
		}
	];
</script>

<div
	class="mx-auto flex h-auto w-full flex-col items-center justify-center bg-[#141415] p-5 py-10
			 text-white md:gap-8 md:px-20 md:py-10 lg:min-h-screen lg:w-11/12 lg:flex-row lg:gap-0"
>
	<div class="w-full space-y-6 lg:w-1/2">
		<h5 class="font-medium uppercase text-blue-700">FAQs</h5>
		<h1 class="text-[35px] font-bold leading-tight md:text-[50px]">
			Got a question?<br class="hidden md:flex" /> Get your answer
		</h1>
		<p class="w-full text-lg text-gray-300 md:w-3/5">
			Quick answers to questions you may have. Can’t find what you’re looking for? Check out our
			full documentation.
		</p>
	</div>

	<div class="mt-5 w-full space-y-6 rounded-xl bg-[#1d1f20] p-6 md:mt-0 lg:w-1/2">
		<div class="space-y-4">
			{#each faqData as faq}
				<Accordion.Root>
					<Accordion.Item value="item-1">
						<Accordion.Trigger>{faq.question}</Accordion.Trigger>
						<Accordion.Content>{faq.answer}</Accordion.Content>
					</Accordion.Item>
				</Accordion.Root>
			{/each}
		</div>
	</div>
</div>
