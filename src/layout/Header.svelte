<script lang="ts">
	type Item = {
		title: string;
		link: string;
	};

	let items: Item[] = [
		{ title: 'Docs', link: 'docs' },
		{ title: 'Components', link: 'components' },
		{ title: 'Themes', link: 'themes' },
		{ title: 'Examples', link: 'examples' },
		{ title: 'Github', link: 'github' }
	];

	import NavItem from '$elements/NavItem.svelte';
	import Theme from '$elements/Theme.svelte';
</script>

<div
	class="sticky top-0 z-50 w-full border-b border-border/40 bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60"
>
	<div class="container flex items-center h-14 max-w-screen-2xl">
		<div class="hidden mr-4 md:flex">
			<a href="/" class="flex items-center mr-6 space-x-2">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 256 256" class="w-6 h-6">
					<rect width="256" height="256" fill="none"></rect>
					<line
						x1="208"
						y1="128"
						x2="128"
						y2="208"
						fill="none"
						stroke="#EB4F27"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="16"
					></line>
					<line
						x1="192"
						y1="40"
						x2="40"
						y2="192"
						fill="none"
						stroke="#EB4F27"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="16"
					></line>
				</svg>
				<span class="hidden font-bold sm:inline-block">shadcn-svelte</span>
			</a>
			<nav class="flex items-center gap-6 text-sm">
				{#each [...items] as item}
					<NavItem title={item.title} link={item.link} />
				{/each}
			</nav>
		</div>
		<div class="flex items-center justify-between flex-1 space-x-2 md:justify-end">
			<div class="flex-1 w-full md:w-auto md:flex-none">
				<button
					type="button"
					tabindex="0"
					class="relative inline-flex items-center justify-start w-full px-4 py-2 text-sm font-medium transition-colors border rounded-md shadow-sm h-9 whitespace-nowrap border-input bg-background text-muted-foreground hover:bg-accent hover:text-accent-foreground focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 sm:pr-12 md:w-40 lg:w-64"
					data-button-root=""
					><span class="hidden lg:inline-flex" data-svelte-h="svelte-1y8n1ih"
						>Search documentation...</span
					> <span class="inline-flex lg:hidden" data-svelte-h="svelte-1fzukxx">Search...</span>
					<kbd
						class="pointer-events-none absolute right-1.5 top-1.5 hidden h-5 select-none items-center gap-1 rounded border bg-muted px-1.5 font-mono text-[10px] font-medium opacity-100 sm:flex"
						data-svelte-h="svelte-1gzgq6m"><span class="text-xs">⌘</span>K</kbd
					></button
				>
			</div>
			<Theme />
		</div>
	</div>
</div>
