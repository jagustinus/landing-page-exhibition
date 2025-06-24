<script lang="ts">
	import * as NavigationMenu from '$lib/components/ui/navigation-menu/index';

	const navigationItems = [
		{
			title: 'Beranda',
			href: '/'
		},
		{
			title: 'Showcase Aplikasi',
			href: '#applications'
		}
	];
</script>

<nav
	class="bg-background supports-[backdrop-filter]:bg-background/60 sticky top-0 z-50 flex w-full flex-1 flex-col border-b px-4 backdrop-blur lg:px-0"
>
	<div class="container mx-auto flex flex-row items-center py-4">
		<NavigationMenu.Root>
			<NavigationMenu.List>
				<NavigationMenu.Item>
					<a href="/" class="mr-4 font-semibold">Exhibition</a>
				</NavigationMenu.Item>
				{#each navigationItems as item}
					<NavigationMenu.Item class="text-muted-foreground">
						<NavigationMenu.Link href={item.href}>{item.title}</NavigationMenu.Link>
					</NavigationMenu.Item>
				{/each}
			</NavigationMenu.List>
		</NavigationMenu.Root>
	</div>
</nav>
