<script lang="ts">
	import { onMount } from 'svelte';
	import { activateOnScroll } from '$lib/util';
	import Milestone3 from '$lib/milestone3.svelte';

	const work = [
		{
			from: '1990',
			to: '1993',
			title: 'BSc Economics with Social Psychology',
			workPlace: 'London School of Economics and Political Science',
			body: '',
			keywords: ['Economics', 'Psychology', 'Statistics'],
			icons: [],
			logo: '/images/lse.gif',
			honors: ''
		},
		{
			from: '1995',
			to: '1997',
			title: "MA Women's Studies",
			workPlace: 'University of Sussex',
			body: '',
			keywords: ['History', 'Literature', 'Sociology', 'Law'],
			icons: [],
			logo: '/images/university-of-sussex.gif',
			honors: 'Summa cum laude'
		},
		{
			from: '1998',
			to: '1999',
			title: 'Postgraduate Certificate in Education',
			workPlace: 'University of Brighton',
			body: 'Confers Qualified Teacher Status (QTS) in the UK, equivalent to a Professional Educator License.',
			keywords: ['Teaching', 'Time Management', 'Organisation'],
			icons: [],
			logo: '',
			honors: ''
		}
	];

	onMount(() => {
		activateOnScroll('.milestone');
	});
</script>

<div
	class="bg-pink-900 py-12">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<div
			class="parallax absolute
			-top-24 right-48 z-0 -mx-96 h-full w-full opacity-50 bg-blend-normal drop-shadow [--parallax-speed:5] sm:right-24 sm:bg-auto md:-right-[10vw] lg:opacity-100">
		</div>
		<a id="work">
			<h2
				class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-200 sm:mb-10">
				// EDUCATION
			</h2>
		</a>
		<div
			class="relative mx-auto space-y-6 overflow-hidden via-90% pb-4 sm:space-y-8 sm:pt-8 sm:before:absolute sm:before:inset-0 sm:before:left-[1px] sm:before:h-full sm:before:w-[1px] sm:before:-translate-x-px sm:before:bg-gradient-to-b sm:before:from-white/25 sm:before:via-white/25 sm:before:to-transparent">
			{#each work as w, i}
				<Milestone3
					from={w.from}
					to={w.to}
					heading={w.title}
					subheading={w.workPlace}
					body={w.body}
					keywords={w.keywords}
					logo={w.logo}
					honors={w.honors}
					active={i === 0}></Milestone3>
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
