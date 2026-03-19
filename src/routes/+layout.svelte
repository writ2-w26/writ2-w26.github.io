<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import '/src/app.css'
	let { children } = $props();
</script>

<svelte:head>
</svelte:head>

{@render children()}
