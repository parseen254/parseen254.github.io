<script>
	import Intro from '$lib/components/Intro.svelte';
	import { siteTitle } from '$lib/config';
</script>

<svelte:head>
	<title>{siteTitle}</title>
</svelte:head>

<Intro />
