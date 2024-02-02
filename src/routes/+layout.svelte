<script lang="ts">
	import '../app.pcss';
	import { ModeWatcher } from 'mode-watcher';
	import Header from '$layout/Header.svelte';
</script>

<div class="flex h-screen w-full flex-col">
	<Header />
	<ModeWatcher />
	<main class="flex-1">
		<div class="border-b">
			<slot />
		</div>
	</main>
</div>
