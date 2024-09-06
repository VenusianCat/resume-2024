<script lang="ts">
	import EditorLine from '$lib/editor-line.svelte';
	import Window from '$lib/window.svelte';

	const skillSets = [
		{
			skillSetHeading: 'Getting Things Done',
			icon: 'fa-check-square',
			description: "I'm deeply pragmatic with a strong bias for action."
		},
		{
			skillSetHeading: 'Bridging Domains',
			icon: 'fa-link',
			description:
				'I\'m curious, analytical and am equally at home with executives and engineers. I enjoy the challenge of aligning praxis with strategy.'
		},
		{
			skillSetHeading: 'Building Teams',
			icon: 'fa-code-branch',
			description:
				'Warm, approachable and egalitarian, with a reputation for capitalizing on individual talents and fostering excellent team dynamics.'
		},
		{
			skillSetHeading: 'Conveying Ideas',
			icon: 'fa-lightbulb',
			description:
				'"Clear, smart, digestible... and highly entertaining"'
		},
		{
			skillSetHeading: 'Designing Systems',
			icon: 'fa-cogs',
			description:
				"From information architecture to process engineering, I've designed and refactored systems of all stripes."
		},
		{
			skillSetHeading: 'Coding',
			icon: 'fa-code',
			description:
				'Full-stack, from SQL to Svelte, since childhood.'
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

<div class="bg-gradient-to-tr from-red-300 via-indigo-400 to-red-300 py-4">
	<div class="relative z-40 mx-auto max-w-7xl px-4 pb-6 pt-6">
		<h2
			class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-200 sm:mb-10">
			// SUPERPOWERS
		</h2>

		<div class="grid gap-4 sm:gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each skillSets as o, i}
				<Window icon={o.icon}>
					<EditorLine class="font-bold text-purple-800/90">
						# {o.skillSetHeading}&nbsp;<!--font awesome icon-->
						<i class="fas {o.icon} text-purple-600"></i>
						&nbsp;
						<!--end font awesome icon-->
					</EditorLine>
					<EditorLine />


					{#each splitStringWithoutBreakingWords(o.description, 40) as s, j}
						<EditorLine class="font-normal text-indigo-800/90">
							{s}
						</EditorLine>
					{/each}

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
