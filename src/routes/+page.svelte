<script lang="ts">
	import Hero from '$lib/sections/hero.svelte';
	import Skills from '$lib/sections/skills.svelte';
	import Work from '$lib/sections/work.svelte';
	import NotWork from '$lib/sections/not-work.svelte';
	import Education2 from '$lib/sections/education2.svelte';
</script>

<Hero />
<div class="relative z-50 h-4 w-full bg-gray-800"></div>
<Work />
<div class="relative z-50 h-4 w-full bg-indigo-900"></div>
<Skills />
<div class="relative z-50 h-4 w-full bg-fuchsia-400"></div>
<NotWork />
<div class="relative z-50 h-4 w-full bg-sky-950"></div>
<Education2 />

<style lang="postcss">

	@keyframes blink {
		0% {
			opacity: 1;
		}
		49% {
			opacity: 1;
		}
		50% {
			opacity: 0;
		}
		100% {
			opacity: 0;
		}
	}

	@keyframes parallax {
		to {
			transform: translateY(calc(var(--parallax-speed) * -200px));
		}
	}

	:global(.parallax) {
		animation: parallax linear;
		animation-timeline: scroll();
	}

	:global(form.dirty input:invalid, form.dirty textarea:invalid) {
		@apply border border-red-500;
	}
</style>
