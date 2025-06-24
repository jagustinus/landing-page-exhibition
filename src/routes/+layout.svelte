<script lang="ts">
	import '../app.css';
	import SectionNavigation from '$lib/components/section-navigation.svelte';

	let { children } = $props();
</script>

<div class="font-geist flex flex-1 flex-col">
	<SectionNavigation />
	<div>
		{@render children()}
	</div>
</div>
