<script lang="ts">
	import EditorLine from '$lib/editor-line.svelte';
	import Window from '$lib/window.svelte';

	const skillSets = [
		{
			skillSetHeading: 'Getting Things Done',
			icon: 'fa-check-square',
			description: "I'm deeply pragmatic and have a strong bias for action."
		},
		{
			skillSetHeading: 'Bridging Domains',
			icon: 'fa-magic',
			description:
				'I speak executive and engineer and I enjoy the challenge of matching praxis to strategic objectives.'
		},
		{
			skillSetHeading: 'Building Teams',
			icon: 'fa-code-branch',
			description:
				'I nurture the creativity that emerges from the diversity of our unique backgrounds and experiences.'
		},
		{
			skillSetHeading: 'Conveying Ideas',
			icon: 'fa-lightbulb',
			description:
				'"Clear, smart, digestible... and highly entertaining"... professional teacher training has ensured zero Powerpoint related deaths since 1998.'
		},
		{
			skillSetHeading: 'Designing Systems',
			icon: 'fa-cogs',
			description:
				"From information architecture to process engineering, I'm deeply fascinated by systems of all stripes."
		},
		{
			skillSetHeading: 'Coding',
			icon: 'fa-code',
			description:
				'Full-stack if not full-time, I know more than enough to be dangerous.'
		}
	];

	function splitStringWithoutBreakingWords(str: string, l: number) {
		var strs = [];
		while (str.length > l) {
			var pos = str.substring(0, l).lastIndexOf(' ');
			pos = pos <= 0 ? l : pos;
			strs.push(str.substring(0, pos));
			var i = str.indexOf(' ', pos) + 1;
			if (i < pos || i > pos + l) i = pos;
			str = str.substring(i);
		}
		strs.push(str);
		return strs;
	}
	let x;
</script>

<div class="bg-gradient-to-tr from-indigo-200 via-red-200 to-slate-100">
	<div class="relative z-40 mx-auto max-w-7xl px-4 pb-6 pt-6">
		<h2
			class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-600 sm:mb-10">
			<span class="text-slate-700">//</span>
			SUPERPOWERS
		</h2>

		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each skillSets as o, i}
				<Window icon={o.icon}>
					<EditorLine class="font-bold text-green-700">
						// &nbsp;<!--font awesome icon-->
						<i class="fas {o.icon} fa-inverse text-green-700"></i>
						&nbsp;
						<!--end font awesome icon-->{o.skillSetHeading}
					</EditorLine>

					<EditorLine class="font-normal text-zinc-300">/*</EditorLine>

					{#each splitStringWithoutBreakingWords(o.description, 35) as s, j}
						<EditorLine class="font-normal text-zinc-900">
							{s}
						</EditorLine>
					{/each}
					<EditorLine class="font-normal text-zinc-300">*/</EditorLine>
				</Window>
			{/each}
		</div>
	</div>
</div>

<style lang="postcss">
	i {
		position: relative;
		top: 0px;
	}
</style>
