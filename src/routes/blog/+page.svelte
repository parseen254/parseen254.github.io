<script>
	import PostsList from '$lib/components/PostsList.svelte'
	import Pagination from '$lib/components/Pagination.svelte'
	import { siteDescription, siteTitle } from '$lib/config'

	export let data
</script>


<svelte:head>
	<title>{siteTitle} | Blog</title>
	<meta data-key="description" name="description" content={siteDescription}>
</svelte:head>
<div class="min-w-full">
	<PostsList posts={data.posts} />
</div>

<Pagination currentPage={1} totalPosts={data.total} />