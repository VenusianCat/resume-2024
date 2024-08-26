<script lang="ts">
	let {
		children,
		icon
	}: {
		children?: any;
		icon?: any;
	} = $props();
</script>

<div class="glass relative z-50 h-fit rounded-lg pb-2 pl-4 shadow-lg backdrop-filter backdrop-blur-sm">
	<div class="counter-reset-line -ml-2 pt-3 text-sm">
		{@render children()}
	</div>
</div>

<style lang="postcss">
	.counter-reset-line {
		counter-reset: line;
	}
	.glass {
		background: rgba(255, 255, 255, 0.3);
		border: 2px solid rgba(255, 255, 255, 0.5);
		padding: 1.25rem;
	}
</style>
