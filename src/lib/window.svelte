<script lang="ts">
	let {
		children,
		icon
	}: {
		children?: any;
		icon?: any;
	} = $props();
</script>

<div class="glass relative z-50 rounded-lg pl-4 shadow-lg backdrop-filter backdrop-blur-sm pt-1 pb-4">
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
	}
</style>
