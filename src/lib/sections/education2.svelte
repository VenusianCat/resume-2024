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
			keywords: ['Economics', 'Psychology', 'Statistics', 'Analysis', 'Critical Thinking', 'Research Design', 'Empathy'],
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
			keywords: ['Critical Thinking and Analysis', 'Intersectional Understanding', 'Empathy and Cultural Sensitivity', 'Research', 'History', 'Literature', 'Sociology', 'Law'],
			icons: [],
			logo: '/images/university-of-sussex.gif',
			honors: 'with distinction / summa cum laude'
		},
		{
			from: '1998',
			to: '1999',
			title: 'Postgraduate Certificate in Education',
			workPlace: 'University of Brighton',
			body: 'Confers Qualified Teacher Status (QTS) in the UK, equivalent to a Professional Educator License.',
			keywords: ['Conveying Information', 'Time Management', 'Organisation', 'Problem Solving', 'Adaptability', 'Resilience', 'Assessment and Evaluation', 'Leadership', 'Instructional Design'],
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
	class="bg-[#3e0819] pt-12 pb-8">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<a id="work">
			<h2
				class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-200">
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
