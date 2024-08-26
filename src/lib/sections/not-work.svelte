<script lang="ts">
	import { onMount } from 'svelte';
	import { activateOnScroll } from '$lib/util';
	import Milestone2 from '$lib/milestone2.svelte';

	const work = [
		{
			from: '2009',
			to: '2016',
			title: 'Blogger',
			workPlace: 'Things to do in Portland with Children',
			body: [
				'For seven years, I wrote and managed Portland\'s leading independent parent-blog, "Things to do in Portland with Children". I blogged about family-friendly activities, events and attractions in the Portland area, and built a community of like-minded parents who shared their own experiences and recommendations. The blog was a great way to combine my passions for fatherhood and photography to support and inspire the busy families around me.'
			],
			keywords: ['Writing', 'Photography', 'Wordpress', 'Community Management'],
			icons: []
		},
		{
			from: '2008',
			to: '2008',
			title: 'Novelist',
			workPlace: 'The Marmalade Shore',
			body: ['My debut (and ultimate) novel , <a class="underline" href="https://www.amazon.com/gp/product/1442138882?ie=UTF8&tag=themarsho-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=1442138882">The Marmalade Shore</a>, was published in 2009 and was a finalist for awards that I hadn\'t heard of either, but yet, staggeringly, didn\'t win any of them.'],
			keywords: ['Writing', 'Perseverance', 'Humility'],
			icons: []
		},
		{
			from: '2000',
			to: '2003',
			title: 'Volunteer Fire Fighter',
			workPlace: 'University of Sussex Response Team',
			body: ['Was part of an first-response team trained to protect lives ahead of professional engagement from the multiplicity of potential hazards on a university campus, including fire, laboratory accidents etc.'],
			keywords: ['First Aid', 'SCBA', 'Firefighting'],
			icons: []
		}
	];

	onMount(() => {
		activateOnScroll('.milestone');
	});
</script>

<div
	class="left-0 -mt-2 w-full overflow-hidden border-t-8 border-slate-700 bg-sky-900 py-6">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<div
			class="parallax absolute
			-top-24 right-48 z-0 -mx-96 h-full w-full opacity-50 bg-blend-normal drop-shadow [--parallax-speed:5] sm:right-24 sm:bg-auto md:-right-[10vw] lg:opacity-100">
		</div>
		<a id="work">
			<h2
				class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-300 sm:mb-10">
				<span class="text-white/50">//</span>
				Extracurricular Activities
			</h2>
		</a>
		<div
			class="relative mx-auto space-y-6 sm:space-y-12 overflow-hidden via-90% pb-4 sm:pt-8 sm:before:absolute sm:before:inset-0 sm:before:left-[1px] sm:before:h-full sm:before:w-[1px] sm:before:-translate-x-px sm:before:bg-gradient-to-b sm:before:from-white/25 sm:before:via-white/25 sm:before:to-transparent">
			{#each work as w, i}
				<Milestone2
					from={w.from}
					to={w.to}
					heading={w.title}
					subheading={w.workPlace}
					body={w.body}
					keywords={w.keywords}
					active={i === 0}></Milestone2>
			{/each}
		</div>
	</div>
</div>

<style lang="postcss">
	@media screen(lg) {
		:global(.milestone.active) {
			transform: translateX(50px);
			transition:
				transform 0.2s ease-out,
				filter 0.2s ease-in,
				opacity 0.2s ease-in;
			opacity: 1;
		}

		:global(.milestone:not(.active)) {
			transform: translateX(0);
			transition:
				transform 0.5s ease-out,
				filter 0.5s ease-in,
				opacity 0.5s ease-in;
			filter: saturate(0%);
			opacity: 0.35;
		}
	}
</style>
