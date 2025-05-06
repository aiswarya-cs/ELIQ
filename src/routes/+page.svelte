<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';
	import Logo1 from '$lib/icons/Logo1.svelte';
	import Logo2 from '$lib/icons/Logo2.svelte';
	import Logo3 from '$lib/icons/Logo3.svelte';
	import Logo4 from '$lib/icons/Logo4.svelte';
	import Logo5 from '$lib/icons/Logo5.svelte';
	import Logo6 from '$lib/icons/Logo6.svelte';
	import { text } from '@sveltejs/kit';
	import BgLines from '$lib/icons/bg-lines.svelte';

	interface product {
		heading: string;
		paragraph: string;
	}

	interface solution {
		image: string;
		head: string;
		description: string;
		buttonText: string;
	}

	interface whatdo {
		text: string;
		colored: string;
		paragraph: string;
	}

	interface faq {
		question: string;
		answer: string;
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
	class="inset-0 min-h-screen w-full bg-[url(images/sierra-saas-gradients.jpg)] bg-cover bg-center bg-no-repeat pb-24 pt-32"
>
	<div class="flex h-[400px] w-full items-center justify-between gap-5 px-36">
		<div class="w-[60%]">
			<h1 class="text-[60px] font-semibold leading-tight text-white">
				Web Eliq – Your Digital<br />Transformation <span class="text-blue-700"><br />Partner</span>
			</h1>
		</div>

		<div class="flex w-[40%] flex-col gap-5">
			<p class="text-xl leading-relaxed text-gray-400">
				Empowering businesses with cutting-edge technology solutions, driving innovation,
				efficiency, and growth. From software development to cloud solutions, IT infrastructure, and
				digital services, we provide end-to-end solutions tailored to your needs.
			</p>
			<button
				type="button"
				class="h-14 w-52 rounded-xl bg-blue-700 text-lg font-medium text-white transition hover:bg-blue-800"
			>
				Get started today
			</button>
		</div>
	</div>

	<div class="flex w-full items-center justify-center p-28">
		<div>
			<img src="images/dashboard.jpg" alt="" srcset="" class="rounded-xl" />
		</div>
	</div>

	<div class="w-full">
		<div class="flex flex-col items-center justify-center gap-5 text-white">
			<h5 class="font-semibold uppercase text-blue-300">what we do</h5>
			<h5 class="text-[50px] font-semibold">Supercharge your business</h5>
			<span class="mb-5 text-center text-lg"
				>Explore tailored products, innovative solutions, and valuable resources <br /> designed to accelerate
				your business growth.</span
			>
		</div>
		<div class="m-6 flex items-center justify-center gap-5">
			<div class="grid grid-cols-1 gap-5 md:grid-cols-2 lg:grid-cols-3">
				{#each ProductData as items}
					<div
						class="flex w-96 flex-col items-start justify-center gap-5 rounded-xl bg-[#1d1f20] p-10 text-white"
					>
						<h1 class="text-3xl font-semibold text-[#ffffff]">{items.heading}</h1>
						<p class="text-gray-500">{items.paragraph}</p>
						<button
							class="h-14 w-52 rounded-xl bg-blue-700 text-lg font-medium text-white hover:border
               hover:border-blue-700 hover:bg-white hover:text-blue-700">view products</button
						>
					</div>
				{/each}
			</div>
		</div>
	</div>

	<div class="mt-32 flex w-full items-center justify-center gap-20">
		<Logo1 data="opacity-10 hover:opacity-80" />
		<Logo5 data="opacity-10 hover:opacity-80" />
		<Logo3 data="opacity-10 hover:opacity-80" />
		<Logo4 data="opacity-10 hover:opacity-80" />
		<Logo2 data="opacity-10 hover:opacity-80" />
		<Logo6 data="opacity-10 hover:opacity-80" />
	</div>
</div>

<div class="relative h-[600px] w-full">
	<div
		class="absolute inset-0 z-0 bg-[url('/images/sierra-saas-video-bg.jpg')] bg-cover bg-center bg-no-repeat"
	></div>
	<div
		class="absolute inset-0 z-10 bg-gradient-to-r from-black/80 via-black/50 to-transparent"
	></div>
	<div
		class="relative z-20 flex h-full flex-col items-center justify-center gap-5 px-4 text-center text-white"
	>
		<h1 class="max-w-3xl text-4xl font-bold md:text-4xl">
			Empower your creativity and craft stunning sites while enjoying real–time customer support at
			every step.
		</h1>
		<a
			href="https://www.youtube.com/embed/VhBl3dHT5SY?feature=oembed?playlist=VhBl3dHT5SY&mute=0&autoplay=0&loop=no&controls=0&start=0&end="
		>
			<button
				class="flex h-16 w-16 items-center justify-center rounded-full bg-white shadow-lg transition hover:scale-105"
			>
				<!-- Play Icon (Tailwind Heroicon - solid play) -->
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-5 w-5 text-black"
					fill="currentColor"
					viewBox="0 0 20 20"
				>
					<path
						fill-rule="evenodd"
						d="M6.5 5.5a1 1 0 011.528-.85l6 4.5a1 1 0 010 1.7l-6 4.5A1 1 0 016.5 14.5v-9z"
						clip-rule="evenodd"
					/>
				</svg>
			</button>
		</a>
	</div>
</div>

<div class="h-auto w-full bg-white">
	<div class="flex flex-col items-center justify-center p-20 text-white">
		<h5 class="font-semibold uppercase text-blue-700">Products</h5>
		<h5 class="text-[50px] font-semibold text-black">Full-cycle software development</h5>
		<span class="mb-5 mt-3 w-2/5 text-center text-lg text-gray-600"
			>Empower your creativity and craft stunning sites effortlessly while enjoying real-time
			customer support at every step.</span
		>

		<div class="mx-20 mt-8 flex w-11/12 items-center justify-center gap-10 text-black">
			<div class="flex w-1/2 flex-col gap-5 rounded-lg bg-[#fafafc] p-10">
				<h1 class="px-3 text-3xl font-semibold">
					AI-driven <span class="text-blue-700"> marketing tools</span>
				</h1>
				<p class="px-3 text-lg text-[#1e1e24b3]">
					Tailored software solutions designed exclusively for your business needs. From efficient
					workflow management to customer engagement tools to drive productivity.
				</p>
				<div class="flex items-center justify-center">
					<img src="images/sierra-saas-6.jpg" alt="" class="rounded-lg" />
				</div>
			</div>
			<div class="flex w-1/2 flex-col gap-5 rounded-lg bg-[#fafafc] p-10">
				<h1 class="px-3 text-3xl font-semibold">
					<span class="text-blue-700">Custom software</span> solutions
				</h1>
				<p class="px-3 text-lg text-[#1e1e24b3]">
					Uncover new opportunities, engage your audience effectively, and achieve remarkable
					results. Empower your brand with intelligent marketing strategies.
				</p>
				<div class="flex items-center justify-center">
					<img src="images/sierra-saas-8.jpg" alt="" class="rounded-lg" />
				</div>
			</div>
		</div>
	</div>
</div>

<div class="h-auto w-full bg-[#fafafc]">
	<div class="flex flex-col items-center justify-center p-20 text-white">
		<h5 class="font-semibold uppercase text-blue-700">Solutions</h5>
		<h5 class="text-center text-[50px] font-semibold leading-tight text-black">
			Every feature you need,<br /> all in a single system
		</h5>
		<span class="mb-5 mt-3 w-2/5 text-center text-lg text-gray-600"
			>Explore a spectrum of solutions meticulously designed to <br /> empower your business growth.</span
		>
		<div class="flex flex-col items-center justify-center p-20 text-white">
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each solutionData as items}
					<div
						class="flex h-full min-h-[320px] w-96 flex-col justify-between rounded-md bg-white p-8 text-black"
					>
						<img src={items.image} alt="" class="h-8 w-8" />
						<div class="mt-5 flex flex-grow flex-col justify-between">
							<div class="flex flex-grow flex-col gap-5">
								<h1 class="text-2xl font-semibold">{items.head}</h1>
								<p class="text-[17px] text-[#5b5b5c]">{items.description}</p>
							</div>
							<button
								class="mt-5 h-10 w-40 rounded-lg bg-[#fafafc] p-2 text-base font-medium text-blue-700"
							>
								{items.buttonText}
							</button>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</div>

<div class="h-auto bg-[#141415] py-10 text-white">
	<div class="flex w-full flex-col items-center justify-center">
		<div class="flex flex-col items-center justify-center gap-2 p-20 text-white">
			<h5 class="font-semibold uppercase text-blue-700">Why Choose Us?</h5>
			<h5 class="text-center text-[50px] font-semibold leading-tight">
				Automate it all, and save hours
			</h5>
			<span class="mb-5 mt-3 w-2/5 text-center text-lg text-gray-400"
				>We bring together everything that’s required to build software. <br /> Reach more customers,
				save time and money, and boost sales.
			</span>
			<div class="mx-20 mt-8 flex w-11/12 items-center justify-center gap-10 text-white">
				<div class="flex w-1/2 flex-col gap-5 rounded-lg bg-[#1d1f20] p-10">
					<h1 class="px-3 text-3xl font-semibold">
						AI-driven <span class="text-blue-700"> marketing tools</span>
					</h1>
					<p class="px-3 text-lg text-[#ffffff]">
						Tailored software solutions designed exclusively for your business needs. From efficient
						workflow management to customer engagement tools to drive productivity.
					</p>
					<div class="my-6 flex items-center justify-center">
						<img src="images/sierra-saas-1.jpg" alt="" class="rounded-lg" />
					</div>
				</div>
				<div class="flex w-1/2 flex-col gap-5 rounded-lg bg-[#1d1f20] p-10">
					<h1 class="px-3 text-3xl font-semibold">
						<span class="text-blue-700">Custom software</span> solutions
					</h1>
					<p class="px-3 text-lg text-[#ffffff]">
						Uncover new opportunities, engage your audience effectively, and achieve remarkable
						results. Empower your brand with intelligent marketing strategies.
					</p>
					<div class="my-6 flex items-center justify-center">
						<img src="images/sierra-saas-2.jpg" alt="" class="rounded-lg" />
					</div>
				</div>
			</div>
		</div>

		<div class="h-[2px] w-4/5 bg-[#282b2c]"></div>

		<div class="flex items-center justify-center py-20">
			<div class="mx-20 grid grid-cols-1 gap-5 md:grid-cols-2 lg:grid-cols-4">
				{#each whatDo as item}
					<div class="flex w-72 flex-col gap-5 rounded-lg bg-[#1d1f20] p-14">
						<h1 class="text-2xl font-medium">
							{item.text} <br /><span class="text-blue-700">{item.colored}</span>
						</h1>
						<p class="font-medium text-[#737474]">{item.paragraph}</p>
					</div>
				{/each}
			</div>
		</div>

		<div class="h-[2px] w-4/5 bg-[#282b2c]"></div>

		<div
			class="mx-auto flex min-h-screen w-11/12 items-center justify-center bg-black px-20 text-white"
		>
			<div class="w-1/2 space-y-6">
				<h5 class="font-medium uppercase text-blue-700">FAQs</h5>
				<h1 class="text-[50px] font-bold leading-tight">
					Got a question? <br />Get your answer
				</h1>
				<p class="w-3/5 text-lg text-gray-300">
					Quick answers to questions you may have. Can’t find what you’re looking for? Check out our
					full documentation.
				</p>
			</div>

			<div class="w-1/2 space-y-6 rounded-xl bg-gray-900 p-6">
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

		<div
			class="relative flex w-full flex-col items-center justify-center overflow-hidden rounded-lg"
		>
			<BgLines data="absolute bg-blue-600 bg-contain bg-center bg-repeat rounded-lg w-4/5 h-auto" />

			<div class="relative z-10 flex flex-col items-center justify-center px-4 py-20 text-center">
				<h1 class="mb-4 text-4xl font-bold text-white md:text-5xl">
					Transform Your Business Today!
				</h1>
				<p class="max-w-2xl text-lg text-white md:text-xl">
					Join hands with Web Eliq and take your business to the next level. Whether you need a
					custom software solution, cloud migration, or a strong digital presence, we are here to
					help.
				</p>

				<div class="mt-8 flex gap-2">
					<input
						type="email"
						placeholder="Email"
						class="rounded-md px-4 py-2 text-black outline-none"
					/>
					<button class="rounded-md bg-black px-4 py-2 text-white">
						Let’s Innovate Together!
					</button>
				</div>
			</div>
		</div>
	</div>
</div>
