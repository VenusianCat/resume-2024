<script lang="ts">
</script>

<code
	class={$$restProps.class +
		" relative block overflow-hidden text-ellipsis whitespace-nowrap break-words font-['Roboto_Mono'] before:mr-4 before:inline-block before:w-6 before:border-r before:border-r-zinc-300/50 before:pr-2 before:text-right before:font-['Roboto_Mono'] before:text-sm before:text-zinc-100/50"}>
	<slot />
</code>

<style lang="postcss">
	code {
		counter-increment: line;
	}

	code::before {
		content: counter(line);
		user-select: none;
		-webkit-user-select: none;
	}
</style>
