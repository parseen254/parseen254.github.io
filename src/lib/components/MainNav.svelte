<script lang="ts">
	import { page } from '$app/stores';
	import DropdownDarkmodeMenu from '$lib/ui/components/DropdownDarkmodeMenu.svelte';
	import { cn } from '$lib/utils.js';
</script>

<div class="mx-auto hidden md:flex">
	<nav class="flex items-center gap-6 text-2xl py-2 px-6 mx-auto">
		<a
			href="/"
			class={cn(
				'hover:text-foreground/80 transition-colors',
				$page.url.pathname === '/docs' ? 'text-foreground' : 'text-foreground/60'
			)}
		>
			Home
		</a>
		<a
			href="/blog"
			class={cn(
				'hover:text-foreground/80 transition-colors',
				$page.url.pathname.startsWith('/docs/components') ? 'text-foreground' : 'text-foreground/60'
			)}
		>
			Blog
		</a>
		<a
			href="/about"
			class={cn(
				'hover:text-foreground/80 transition-colors',
				$page.url.pathname.startsWith('/docs/components') ? 'text-foreground' : 'text-foreground/60'
			)}
		>
			About
		</a>
		<a
			href="/contact"
			class={cn(
				'hover:text-foreground/80 transition-colors',
				$page.url.pathname.startsWith('/themes') ? 'text-foreground' : 'text-foreground/60'
			)}
		>
			Contact
		</a>
		<div class="ml-8">
			<DropdownDarkmodeMenu />
		</div>
	</nav>
</div>
