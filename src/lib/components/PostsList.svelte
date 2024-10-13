<script>
	import { cn } from '$lib/utils.js';
	export let posts = [];
</script>

<ul class="flex flex-row flex-wrap gap-6">
	{#each posts as post}
		<li class="rounded-md">
			<article>
				<a href="/blog/{post.slug}">
					<img
						class={cn(
							'max-w-[250px] mb-4 object-cover transition-all hover:scale-105',
							'aspect-[3/4]'
						)}
						src={post.coverImage}
						alt={post.title}
					/>
					<h4 class="max-w-[250px] font-bold">
						{post.title}
					</h4>
					<p class="max-w-[250px]">{post.excerpt}</p>
				</a>
			</article>
		</li>
	{/each}
</ul>
