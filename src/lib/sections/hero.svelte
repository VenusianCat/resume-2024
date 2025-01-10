<script>
	import LinkedIn from '$lib/icons/linked-in.svelte';
	import { base } from '$app/paths';
</script>

<div
	class="w-full flex-col justify-start overflow-hidden sm:bg-[url('/images/headshot-2.jpg')] sm:bg-cover sm:bg-right sm:bg-no-repeat">
	<!--author block, non-mobile-->
	<div class="hidden px-4 py-6 text-5xl sm:block">
		<p class="font-['Roboto_Mono'] tracking-wide text-slate-100/90">
			<span class="text-slate-400/20">&gt;</span>Richard Tammar<span
				class="text-slate-400">_</span>
		</p>
	</div>
	<!--author block, mobile-->
	<h1
		class="bg-sky-100 px-2 pt-2 font-['Roboto_Mono'] text-2xl tracking-wide text-slate-900 sm:hidden">
		<span class="text-sky-300">&gt;&nbsp;</span>Richard Tammar<span
			class="text-sky-300">_</span>
	</h1>

	<div class="bg-slate-500 sm:hidden">
		<svg
			xmlns="http://www.w3.org/2000/svg"
			viewBox="0 0 1000 100"
			fill="#e0f2fe">
			<path
				d="M0 0v90.2C49.7 99.9 105 82 160 65c75.5-23.3 145.5-22.4 222-3 63 16 119 14 173-8 79.5-32.4 156.2-27.6 240-10 82.6 17.4 143-1 205-31.7V0H0Z">
			</path>
		</svg>
	</div>

	<p
		class="bg-slate-500 pb-8 pl-4 sm:pl-12 pr-3 pt-2 font-['Roboto_Mono'] text-slate-100/90 sm:max-w-[30rem] sm:bg-transparent sm:text-xl md:max-w-[42rem]">
		<img
			src="{base}/images/headshot-square.jpg"
			alt="headshot of Richard Tammar"
			class="visible float-right ml-1 mb-1 mr-2 size-24 rounded-full sm:hidden" />
		Veteran technologist with a knack for connecting the C-suite to the engine room.
		Empathetic, curious and analytical, I work to catalyze positive change.
	</p>

	<div class="absolute right-2 top-1 text-slate-700">
		<a
			href="https://www.linkedin.com/in/richardtammar/"
			class="-mr-1 block h-12 w-12 p-1">
			<LinkedIn />
		</a>
	</div>
</div>

<style lang="postcss">
</style>
