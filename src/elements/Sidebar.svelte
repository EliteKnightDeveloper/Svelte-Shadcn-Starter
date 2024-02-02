<script lang="ts">
	export let title: string = '';
	type SidebarItem = {
		link: string;
		content: string;
	};
	export let items: SidebarItem[] = [];
</script>

<div class="pb-4">
	<h4 class="mb-1 rounded-md px-2 py-1 text-sm font-semibold">{title}</h4>
	<div class="grid grid-flow-row auto-rows-max text-sm">
		{#each [...items] as item}
			<a
				href="/{item.link}"
				class="group flex w-full items-center rounded-md border border-transparent px-2 py-1 text-muted-foreground hover:underline"
			>
				{item.content}
			</a>
		{/each}
	</div>
</div>
