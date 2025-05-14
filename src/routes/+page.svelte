<script lang="ts">
	import Faq from '$lib/components/Faq.svelte';
	import Logo from '$lib/components/Logo.svelte';
	import WhatDo from '$lib/components/WhatDo.svelte';
	import PlayCard from '$lib/components/PlayCard.svelte';
	import ContactUs from '$lib/components/ContactUs.svelte';
	import HeroSection from '$lib/components/HeroSection.svelte';
	import WhyChooseUs from '$lib/components/WhyChooseUs.svelte';
	import ProductCard from '$lib/components/Product_Card.svelte';
	import HorizontalLine from '$lib/components/HorizontalLine.svelte';
	import ProductSection from '$lib/components/ProductSection.svelte';
	import SolutionDataCard from '$lib/components/SolutionDataCard.svelte';
</script>

<div
	class="inset-0 min-h-screen w-full bg-[url(images/sierra-saas-gradients.jpg)] bg-cover bg-center
 bg-no-repeat pb-10 pt-28 md:pb-24 md:pt-32"
>
	<HeroSection />
	<div class="mt-10 flex w-full items-center justify-center px-4 sm:px-6 md:py-16 lg:px-36">
		<div class="w-full max-w-screen-xl">
			<img src="images/dashboard.jpg" alt="dashboard" class="w-full rounded-xl object-cover" />
		</div>
	</div>

	<div class="mt-16 w-full px-4 sm:px-6 md:px-8 lg:px-36">
		<div class="flex flex-col items-center gap-4 text-center text-white">
			<h5 class="font-semibold uppercase text-blue-300">what we do</h5>
			<h2 class="text-3xl font-semibold leading-tight md:text-4xl lg:text-5xl">
				Supercharge your business
			</h2>
			<p class="text-base text-gray-300 md:text-lg">
				Explore tailored products, innovative solutions, and valuable resources
				<br class="hidden md:inline" />
				designed to accelerate your business growth.
			</p>
		</div>

		<ProductCard />
	</div>

	<div
		class="mt-3 flex w-full items-center justify-center gap-2 p-5 md:mt-32 md:flex md:gap-20 md:p-0"
	>
		<Logo />
	</div>
</div>

<PlayCard />

<div class="h-auto w-full bg-white">
	<ProductSection />
</div>

<div class="w-full bg-[#fafafc]">
	<div class="flex flex-col items-center justify-center px-4 py-8 lg:px-20 lg:py-20">
		<div class="flex flex-col items-center px-2 text-center md:px-0">
			<h5 class="font-semibold uppercase text-blue-700">Solutions</h5>
			<h5
				class="text-[28px] font-semibold leading-tight text-black sm:text-[36px] md:text-[44px] lg:text-[50px]"
			>
				Every feature you need,<br class="hidden md:block" />
				all in a single system
			</h5>
			<span class="mb-5 mt-3 text-base text-gray-600 sm:text-lg">
				Explore a spectrum of solutions meticulously designed to <br class="hidden md:block" />
				empower your business growth.
			</span>
		</div>
		<SolutionDataCard />
	</div>
</div>

<div class="h-auto bg-[#141415] py-10 text-white">
	<div class="flex w-full flex-col items-center justify-center">
		<!-- why choose us-->
		<WhyChooseUs />
		<HorizontalLine data="h-[2px] w-4/5 bg-[#282b2c]" />
		<WhatDo />
		<HorizontalLine data="mt-5 h-[2px] w-4/5 bg-[#282b2c] md:mt-0" />
		<Faq />
		<ContactUs />
	</div>
</div>
