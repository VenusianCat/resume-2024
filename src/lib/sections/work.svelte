<script lang="ts">
	import AzureAiStudio from '$lib/icons/azure-ai-studio.svelte';
	import AzureDevops from '$lib/icons/azure-devops.svelte';
	import AzureFunctions from '$lib/icons/azure-functions.svelte';
	import AzureSql from '$lib/icons/azure-sql.svelte';
	import Azure from '$lib/icons/azure.svelte';
	import Cosmos from '$lib/icons/cosmos.svelte';
	import DotNet from '$lib/icons/dot-net.svelte';
	import OpenAi from '$lib/icons/open-ai.svelte';
	import Milestone from '$lib/milestone.svelte';
	import Javascript from '$lib/icons/javascript.svelte';
	import Typescript from '$lib/icons/typescript.svelte';
	import React from '$lib/icons/react.svelte';
	import Docker from '$lib/icons/docker.svelte';
	import Redis from '$lib/icons/redis.svelte';
	import Angular from '$lib/icons/angular.svelte';
	import SqlServer from '$lib/icons/sql-server.svelte';
	import Powershell from '$lib/icons/powershell.svelte';
	import Jquery from '$lib/icons/jquery.svelte';
	import C from '$lib/icons/c.svelte';
	import { onMount } from 'svelte';
	import { activateOnScroll } from '$lib/util';

	const work = [
		{
			from: '2012',
			to: 'Present',
			title: 'Senior Director of Digital Strategy',
			workPlace: 'Travel Portland',
			locationDescription:
				"Travel Portland is recognized as one of the most innovative and effective Destination Marketing Organizations in the United States and is a significant contributor to the city's $6bn tourism sector.",
			body: [
				"I lead the organization's digital strategy and direct its core products – including the multi-award-winning TravelPortland.com and Near Me Now. Additionally, I chair the company's Systems Integration Team and direct a team of internal and external specialists, SMEs and service providers."
			],
			keywords: [
				'Team Leadership',
				'Platform Architecture',
				'Systems Architecture',
				'WordPress',
				'JavaScript',
				'PHP',
				'SQL (MySQL, MSSQL)',
				'JIRA',
				'git'
			],
			icons: [
				DotNet,
				Azure,
				Cosmos,
				AzureSql,
				AzureDevops,
				AzureFunctions,
				AzureAiStudio,
				OpenAi
			]
		},
		{
			from: '2008',
			to: '2012',
			title: 'Director of Web Development',
			workPlace: 'One Economy Corporation',
			locationDescription:
				'One Economy Corporation was a Washington, D.C.-based, global nonprofit that connected underserved communities around the world to the internet and tailor-made informational resources.',
			body: [
				'I directed the Web Development and Product Management verticals of the Media Division, with up to 17 reports, and provided technical leadership across such initiatives as The Public Internet Channel, The Beehive and Applications for Good, with a combined traffic in excess of 1M unique visitors per month.'
			],
			keywords: [
				'Team Leadership',
				'Platform Architecture',
				'Systems Architecture',
				'WordPress',
				'Drupal',
				'JavaScript',
				'PHP',
				'SQL (MySQL, MSSQL)',
				'JIRA',
				'C#'
			],
			icons: [
				DotNet,
				Typescript,
				Javascript,
				React,
				Redis,
				AzureSql,
				AzureDevops,
				Docker
			]
		},
		{
			from: '2004',
			to: '2008',
			title: 'Web Manager',
			workPlace: 'Lattice Semiconductor',
			locationDescription:
				'Lattice Semiconductor Corporation (NASDAQ: LSCC) designs high-performance programmable logic devices with annual revenues of around $600M.',
			body: [
				"I directed the corporation's global web presence, intranet, extranet and email marketing programs. I managed the web team and reengineered the corporate web site, significantly enhancing customer-satisfaction, usability, lead generation and organic search rank; significantly reducing support and maintenance overheads and marketing lead times."
			],
			keywords: [
				'Content Management Systems',
				'Platform Architecture',
				'Team Leadership',
				'SEO',
				'Email Marketing',
				'SQL (Oracle, MySQL)',
				'PHP',
				'Coldfusion'
			],
			icons: [
				DotNet,
				Typescript,
				Javascript,
				Angular,
				SqlServer,
				Redis,
				Powershell
			]
		},
		{
			from: '1999',
			to: '2004',
			title: 'Web Manager',
			workPlace: 'University of Sussex',
			locationDescription:
				'The University of Sussex is a leading British public research university.',
			body: [
				"I was responsible for the University's web presence, ran technical lead on all major web development initiatives and line managed the University web team. We built a campus-wide content management system, enabling non-technical staff in 100+ subordinate units to maintain an independent departmental website while maintaining consistent institutional branding and a unified UX. The CMS integrated with HR and curriculum systems to ensure currency of staff data, program specifications et al. Through so doing we increased usability, reduced technical overheads and cut support costs."
			],
			keywords: [
				'Team Leadership',
				'Platform Architecture',
				'Content Management Systems',
				'UX',
				'SQL (Oracle, MySQL)',
				'Coldfusion',
				'PHP',
				'HTML'
			],
			icons: [DotNet, Azure, Typescript, Javascript, Angular, React, SqlServer]
		}
	];

	onMount(() => {
		activateOnScroll('.milestone');
	});
</script>

<div
	class="left-0 -mt-2 w-full overflow-hidden border-t-8 border-slate-700 bg-slate-800 py-6">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<div
			class="parallax absolute
			-top-24 right-48 z-0 -mx-96 h-full w-full bg-[url('/images/keyboard.webp')] bg-contain bg-no-repeat opacity-50 bg-blend-normal drop-shadow [--parallax-speed:5] sm:right-24 sm:bg-auto md:-right-[10vw] lg:opacity-100">
		</div>
		<a id="work">
			<h2
				class="relative z-10 mx-auto mb-10 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-300">
				<span class="text-white/50">//</span>
				EXPERIENCE
			</h2>
		</a>
		<div
			class="relative mx-auto space-y-12 overflow-hidden via-90% pb-4 sm:pt-8 sm:before:absolute sm:before:inset-0 sm:before:left-[1px] sm:before:h-full sm:before:w-[1px] sm:before:-translate-x-px sm:before:bg-gradient-to-b sm:before:from-white/25 sm:before:via-white/25 sm:before:to-transparent">
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
