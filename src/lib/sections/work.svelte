<script lang="ts">
	import { onMount } from 'svelte';
	import { activateOnScroll } from '$lib/util';
	import Milestone from '$lib/milestone.svelte';

	const work = [
		{
			from: '2012',
			to: 'Present',
			title: 'Senior Director of Digital Strategy',
			workPlace: 'Travel Portland',
			locationDescription:
				"Travel Portland is recognized as an industry leading Destination Marketing Organizations in the United States and is the primary driver of the city's $6bn tourism sector.",
			body: [
				'I am responsible for Travel Portland\'s digital strategy, systems and products, including the multi-award-winning <a class="underline" href="https://travelportland.com">TravelPortland.com</a> and the <a class="underline" href="https://apps.apple.com/us/app/portland-near-me-now/id1661418385">Near Me Now</a> mobile app. I chair the Systems Integration Team and direct a wide array of technical specialists.'
			],
			keywords: [
				'Strategic Alignment',
				'Team Leadership',
				'Systems Architecture',
				'Product Management',
				'WordPress',
				'Simpleview CRM',
				'JavaScript',
				'PHP',
				'SQL',
				'JIRA',
				'git'
			],
			icons: []
		},
		{
			from: '2008',
			to: '2012',
			title: 'Director of Web Development',
			workPlace: 'One Economy Corporation',
			locationDescription:
				'In 2012, One Economy Corporation was a US-based nonprofit that connected underserved communities around the globe to the internet and tailor-made informational resources.',
			body: [
				'I directed the Web Development and Product Management verticals of the Media Division, and provided technical leadership for <i>The Public Internet Channel</i> and <i>Applications for Good</i>, with a combined traffic in excess of 1M unique visitors per month.'
			],
			keywords: [
				'Strategic Alignment',
				'Team Leadership',
				'Systems Architecture',
				'WordPress',
				'Drupal',
				'JavaScript',
				'PHP',
				'SQL',
				'JIRA',
				'C#',
				'HTML',
				'CSS',
				'SVN',
				'git'
			],
			icons: []
		},
		{
			from: '2004',
			to: '2008',
			title: 'Web Manager',
			workPlace: 'Lattice Semiconductor Corporation',
			locationDescription:
				'Lattice Semiconductor Corporation (NASDAQ: LSCC) designs high-performance programmable logic devices.',
			body: [
				"I directed the corporation's global web presence, intranet, extranet and email marketing programs. I managed the web team and reengineered the corporate web site, enhancing usability, lead generation and organic search rank while reducing maintenance overheads and marketing lead times."
			],
			keywords: [
				'Content Management Systems',
				'Platform Architecture',
				'Team Leadership',
				'SEO',
				'Email Marketing',
				'SQL',
				'PHP',
				'Coldfusion',
				'HTML',
				'CSS'
			],
			icons: []
		},
		{
			from: '1999',
			to: '2004',
			title: 'Web Manager',
			workPlace: 'University of Sussex',
			locationDescription:
				'The University of Sussex is a leading British public research university.',
			body: [
				"I was responsible for the university's web presence and managed the core web team. We were one of the very first universities to develop and implement a campus-wide content management system, enabling non-technical staff in over 100 departments to maintain an independent website within a unified UX. Our CMS integrated with HR and curriculum systems to ensure currency of staff data, program specifications <i>et al</i>. Through so doing we increased usability, reduced technical overheads and cut support costs."
			],
			keywords: [
				'Team Leadership',
				'Platform Architecture',
				'Content Management Systems',
				'UX',
				'SQL',
				'Coldfusion',
				'PHP',
				'HTML'
			],
			icons: []
		}
	];

	onMount(() => {
		activateOnScroll('.milestone');
	});
</script>

<div class="left-0 -mt-2 w-full overflow-hidden bg-slate-800 py-6 md:py-8">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<a id="work">
			<h2
				class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-300">
				<span class="text-white/50">//</span>
				WORK EXPERIENCE
			</h2>
		</a>
		<div
			class="relative mx-auto space-y-6 overflow-hidden via-90% pb-4 sm:space-y-12 sm:pt-8 sm:before:absolute sm:before:inset-0 sm:before:left-[1px] sm:before:h-full sm:before:w-[1px] sm:before:-translate-x-px sm:before:bg-gradient-to-b sm:before:from-white/25 sm:before:via-white/25 sm:before:to-transparent">
			{#each work as w, i}
				<Milestone
					from={w.from}
					to={w.to}
					heading={w.title}
					subheading={w.workPlace}
					preamble={w.locationDescription}
					body={w.body}
					keywords={w.keywords}
					active={i === 0}></Milestone>
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
