<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Sun, Moon } from 'radix-icons-svelte';
	import { toggleMode } from 'mode-watcher';
</script>

<Button on:click={toggleMode} variant="outline" size="icon" class="w-8 h-8 border-none">
	<Sun
		class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
	/>
	<Moon
		class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
	/>
</Button>
