<script lang="ts">
	export let title: string = '';
	export let link: string = '';
</script>

<a href="/{link}" class="text-foreground/60 transition-colors hover:text-foreground/80">{title}</a>
