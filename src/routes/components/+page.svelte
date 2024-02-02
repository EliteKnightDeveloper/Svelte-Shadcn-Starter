<script lang="ts">
	import Sidebar from '$elements/Sidebar.svelte';

	type SidebarItem = {
		link: string;
		content: string;
	};
	type Sidebar = {
		title: string;
		items: SidebarItem[];
	};

	let sidebars: Sidebar[] = [
		{
			title: 'Getting Started',
			items: [
				{ link: 'introduction', content: 'Introduction' },
				{ link: 'install', content: 'Installation' },
				{ link: 'componet', content: 'Component.json' },
				{ link: 'theme', content: 'Theming' },
				{ link: 'dark', content: 'Dark mode' },
				{ link: 'cli', content: 'CLI' },
				{ link: 'typo', content: 'Typography' },
				{ link: 'figma', content: 'Figma' },
				{ link: 'changelog', content: 'Changelog' },
				{ link: 'about', content: 'About' }
			]
		},
		{
			title: 'Components',
			items: [
				{ link: 'accordion', content: 'Accordion' },
				{ link: 'alert', content: 'Alert' },
				{ link: 'alertdialog', content: 'Alert Dialog' },
				{ link: 'aspect', content: 'Aspect Ratio' }
			]
		}
	];
</script>

<div
	class="container flex-1 items-start md:grid md:grid-cols-[220px_minmax(0,1fr)] md:gap-6 lg:grid-cols-[240px_minmax(0,1fr)] lg:gap-10"
>
	<div
		class="scrollbar-thin fixed top-14 z-30 -ml-2 hidden h-[calc(100vh-3.5rem)] w-full shrink-0 overflow-y-auto md:sticky md:block"
	>
		<div class="h-full py-6 pr-6 lg:py-8">
			<div class="w-full">
				{#each [...sidebars] as sidebar}
					<Sidebar title={sidebar.title} items={sidebar.items} />
				{/each}
			</div>
		</div>
	</div>
	<div class="relative py-6 lg:gap-10 lg:py-8 xl:grid xl:grid-cols-[1fr_300px]">
		<div class="mx-auto w-full min-w-0"></div>
		<div class="hidden text-sm xl:block">
			<div class="sticky top-16 h-[calc(100vh-3.5rem)] overflow-hidden">
				<div class="space-y-2">
					<p class="font-medium">On This Page</p>
					<ul class="m-0 list-none">
						<li class="mt-0 pt-2">
							<a
								href="#installation"
								class="inline-block font-medium text-foreground no-underline transition-colors hover:text-foreground"
								>Installation</a
							>
						</li>
						<li class="mt-0 pt-2">
							<a
								href="#usage"
								class="inline-block text-muted-foreground no-underline transition-colors hover:text-foreground"
								>Usage</a
							>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>
