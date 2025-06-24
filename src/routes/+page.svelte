<script lang="ts">
	import Hero from '$lib/components/hero.svelte';
	import SectionApplication from '$lib/components/section-application.svelte';
	import Footer from '$lib/components/footer.svelte';
</script>

<svelte:head>
	<title>Exhibition</title>
</svelte:head>

<div class="relative flex min-h-screen flex-col">
	<main>
		<Hero />
		<SectionApplication />
	</main>
	<Footer />
</div>
