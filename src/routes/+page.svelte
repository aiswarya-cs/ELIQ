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

	const logos = [Logo1, Logo2, Logo3, Logo4, Logo5, Logo6];
</script>

<div class="inset-0 min-h-screen w-full bg-[url(images/sierra-saas-gradients.jpg)] bg-cover bg-center bg-no-repeat pb-10 pt-28 md:pt-32 md:pb-24">
  <!-- Hero Section -->
  <div class="w-full flex flex-col items-center justify-between gap-10 px-4 sm:px-6 lg:flex-row lg:px-40">
    <!-- Left Content -->
    <div class="w-full lg:w-[60%]">
      <h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-semibold leading-tight text-white">
        Web Eliq – Your Digital
        <br class="hidden lg:block" />
        Transformation <span class="text-blue-700"><br />Partner</span>
      </h1>
    </div>

    <!-- Right Content -->
    <div class="w-full lg:w-[40%] mt-5 lg:mt-0 flex flex-col gap-5">
      <p class="text-base sm:text-lg leading-relaxed text-gray-300">
        Empowering businesses with cutting-edge technology solutions, driving innovation,
        efficiency, and growth. From software development to cloud solutions, IT infrastructure, and
        digital services, we provide end-to-end solutions tailored to your needs.
      </p>
      <button
        type="button"
        class="h-12 w-48 rounded-xl bg-blue-700 text-base font-medium text-white transition hover:bg-blue-800"
      >
        Get started today
      </button>
    </div>
  </div>

  <!-- Image Section -->
  <div class="mt-10 flex w-full items-center justify-center px-4 sm:px-6 md:py-16 lg:px-36">
    <div class="w-full max-w-screen-xl">
      <img
        src="images/dashboard.jpg"
        alt="dashboard"
        class="w-full rounded-xl object-cover"
      />
    </div>
  </div>

  <!-- What We Do Section -->
  <div class="w-full px-4 sm:px-6 md:px-8 lg:px-36 mt-16">
    <div class="flex flex-col items-center text-center gap-4 text-white">
      <h5 class="text-blue-300 font-semibold uppercase">what we do</h5>
      <h2 class="text-3xl md:text-4xl lg:text-5xl font-semibold leading-tight">
        Supercharge your business
      </h2>
      <p class="text-base md:text-lg text-gray-300">
        Explore tailored products, innovative solutions, and valuable resources
        <br class="hidden md:inline" />
        designed to accelerate your business growth.
      </p>
    </div>

    <!-- Product Cards -->
    <div class="mt-10 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      {#each ProductData as items}
        <div class="bg-[#1d1f20] p-8 rounded-xl flex flex-col gap-4 text-white w-full">
          <h3 class="text-2xl font-semibold">{items.heading}</h3>
          <p class="text-gray-400">{items.paragraph}</p>
          <button class="h-12 w-48 rounded-xl bg-blue-700 text-base font-medium hover:bg-white hover:text-blue-700 hover:border hover:border-blue-700">
            View products
          </button>
        </div>
      {/each}
    </div>
  </div>


	<!-- <div class="md:mt-32  mt-3 flex w-full items-center justify-center gap-2 p-5 md:p-0 md:gap-20 md:flex">
		<Logo1 data="opacity-10 hover:opacity-80" />
		<Logo5 data="opacity-10 hover:opacity-80" />
		<Logo3 data="opacity-10 hover:opacity-80" />
		<Logo4 data="opacity-10 hover:opacity-80" />
		<Logo2 data="opacity-10 hover:opacity-80" />
		<Logo6 data="opacity-10 hover:opacity-80" />
	</div> -->
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

<!-- <div class="h-auto w-full bg-white">
	<div class="flex flex-col items-center justify-center px-5 py-10 text-white md:p-20">
		<h5 class="font-semibold uppercase text-blue-700">Products</h5>
		<h5 class="text-center text-[35px] font-semibold leading-tight text-black md:text-[50px]">
			Full-cycle software development
		</h5>
		<span class="mb-5 mt-3 w-full text-center text-lg text-gray-600 md:w-2/5"
			>Empower your creativity and craft stunning sites effortlessly while enjoying real-time
			customer support at every step.</span
		>

		<div
			class="mt-8 flex w-11/12 flex-col items-center justify-center gap-10 text-black md:mx-20 md:flex-row"
		>
			<div class="flex w-full flex-col gap-5 rounded-lg bg-[#fafafc] md:w-1/2 md:p-10">
				<h1 class="text-[28px] font-semibold md:px-3 md:text-3xl">
					<span class="text-blue-700">Custom software</span> solutions
				</h1>
				<p class="text-lg text-[#1e1e24b3] md:px-3">
					Uncover new opportunities, engage your audience effectively, and achieve remarkable
					results. Empower your brand with intelligent marketing strategies.
				</p>
				<div class="flex items-center justify-center">
					<img src="images/sierra-saas-8.jpg" alt="" class="rounded-lg" />
				</div>
			</div>

			<div class="flex w-full flex-col gap-5 rounded-lg bg-[#fafafc] md:w-1/2 md:p-10">
				<h1 class="text-[28px] font-semibold md:px-3 md:text-3xl">
					AI-driven <span class="text-blue-700"> marketing tools</span>
				</h1>
				<p class="text-lg text-[#1e1e24b3] md:px-3">
					Tailored software solutions designed exclusively for your business needs. From efficient
					workflow management to customer engagement tools to drive productivity.
				</p>
				<div class="flex items-center justify-center">
					<img src="images/sierra-saas-6.jpg" alt="" class="rounded-lg" />
				</div>
			</div>
		</div>
	</div>
</div> -->

<!-- <div class="h-auto w-full bg-[#fafafc]">
	<div class="flex flex-col items-center justify-center p-5 text-white md:p-20">
		<div class="flex flex-col items-center justify-center p-2 md:p-0">
			<h5 class="font-semibold uppercase text-blue-700">Solutions</h5>
			<h5 class="text-center text-[32px] font-semibold leading-tight text-black md:text-[50px]">
				Every feature you need,<br class="hidden md:flex" /> all in a single system
			</h5>
			<span class="mb-5 mt-3 w-full text-center text-lg text-gray-600"
				>Explore a spectrum of solutions meticulously designed to <br class="hidden md:flex" /> empower
				your business growth.</span
			>
		</div>

		<div class="flex flex-col items-center justify-center p-5 text-white md:p-20">
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each solutionData as items}
					<div
						class="flex h-full min-h-[320px] w-full flex-col justify-between rounded-md bg-white
						 p-5 text-black md:w-96 md:p-8"
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
</div> -->

<div class="h-auto bg-[#141415] py-10 text-white">
	<div class="flex w-full flex-col items-center justify-center">
		<!-- <div class="flex flex-col items-center justify-center gap-2 p-5 text-white md:p-20">
			<h5 class="font-semibold uppercase text-blue-700">Why Choose Us?</h5>
			<h5 class="text-center text-[30px] font-semibold leading-tight md:text-[50px]">
				Automate it all, and save hours
			</h5>
			<span class="mb-5 mt-3 w-full px-4 text-center text-lg text-gray-400 md:w-2/5"
				>We bring together everything that’s required to build software. <br
					class="hidden md:flex"
				/> Reach more customers, save time and money, and boost sales.
			</span>

			<div
				class="mt-8 flex flex-col items-center justify-center gap-10 text-white md:mx-20 md:flex-row md:w-11/12"
			>
				<div class="flex w-full flex-col gap-5 rounded-lg bg-[#1d1f20] p-5 md:w-1/2 md:p-10">
					<h1 class="px-3 text-3xl font-semibold">
						Cloud computing <span class="text-blue-700"> infrastructure</span>
					</h1>
					<p class="px-3 text-lg text-[#ffffff]">
						Lower cost, greater efficiency, faster deployment and more innovation. Increases service
						levels, reduces service outages and improve the customer experience.
					</p>
					<div class="my-6 flex items-center justify-center">
						<img src="images/sierra-saas-1.jpg" alt="" class="rounded-lg" />
					</div>
				</div>

				<div class="flex w-full flex-col gap-5 rounded-lg bg-[#1d1f20] p-5 md:w-1/2 md:p-10">
					<h1 class="px-3 text-3xl font-semibold">
						<span class="text-blue-700">Performance and</span> optimization
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
		</div> -->

		<div class="h-[2px] w-4/5 bg-[#282b2c]"></div>
<!-- 
		<div class="flex items-center justify-center py-5 md:py-20">
			<div class="mx-5 grid grid-cols-1 gap-5 md:mx-20 md:grid-cols-2 lg:grid-cols-4">
				{#each whatDo as item}
					<div class="flex w-full flex-col gap-5 rounded-lg bg-[#1d1f20] p-5 md:w-72 md:p-14">
						<h1 class="text-2xl font-medium">
							{item.text} <br class="hidden md:flex" />
							<span class="text-blue-700">{item.colored}</span>
						</h1>
						<p class="font-medium text-[#737474]">{item.paragraph}</p>
					</div>
				{/each}
			</div>
		</div>

		<div class="h-[2px] w-4/5 bg-[#282b2c] mt-5 md:mt-0"></div>

		<div
			class="mx-auto flex flex-col md:flex-row h-auto md:min-h-screen w-full items-center
			 justify-center bg-[#141415] p-5 py-10 md:py-0 text-white md:w-11/12 md:px-20"
		>
			<div class="w-full space-y-6 md:w-1/2">
				<h5 class="font-medium uppercase text-blue-700">FAQs</h5>
				<h1 class="text-[35px] md:text-[50px] font-bold leading-tight">
					Got a question?<br class="hidden md:flex" /> Get your answer
				</h1>
				<p class="w-full text-lg text-gray-300 md:w-3/5">
					Quick answers to questions you may have. Can’t find what you’re looking for? Check out our
					full documentation.
				</p>
			</div>

			<div class="w-full mt-5 md:mt-0 md:w-1/2 space-y-6 rounded-xl bg-[#1d1f20] p-6">
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
		</div> -->

		<!-- <div
			class="relative flex w-full flex-col items-center justify-center overflow-hidden rounded-lg"
		>
			<BgLines data="absolute bg-blue-600 bg-contain bg-center bg-repeat rounded-lg w-full md:w-4/5 py-20 h-auto" />

			<div class="relative z-10 flex flex-col items-center justify-center px-4 py-20 text-center">
				<h1 class="mb-4 text-3xl font-bold text-white md:text-5xl">
					Transform Your Business Today!
				</h1>
				<p class="max-w-2xl text-lg text-white md:text-xl">
					Join hands with Web Eliq and take your business to the next level. Whether you need a
					custom software solution, cloud migration, or a strong digital presence, we are here to
					help.
				</p>

				<div class="md:mt-8 mt-5 flex-col md:flex-row gap-2">
					<input
						type="email"
						placeholder="Email"
						class="rounded-md w-96 md:w-auto px-4 py-2 text-black outline-none"
					/>
					<button class="rounded-md w-52 md:w-auto bg-black px-4 py-2 mt-5 md:mt-0 text-white">
						Let’s Innovate Together!
					</button>
				</div>
			</div>
		</div> -->
	</div>
</div>
