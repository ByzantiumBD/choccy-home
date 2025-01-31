<script lang="ts">
	import Background from '$lib/components/common/background.svelte';
	import '@fontsource/roboto';
	import '../app.less';
	import { page } from '$app/state';
	import Footer from '$lib/components/home/footer.svelte';
	import Header from '$lib/components/common/header.svelte';
	import { onMount } from 'svelte';
	import Spinner from '$lib/components/common/spinner.svelte';

	let { children } = $props();

	let isHome = $derived(page.url.pathname === "/");
	let loading = $state(false)

	onMount(async () => {
		if (!isHome) loading = true;
		loading = false;
	})
</script>

<div class="overflow-hidden relative bg-black min-h-screen flex flex-col justify-between">
	<Header />

	<Background>
		{#if loading}
			<Spinner />
		{:else}
			{@render children()}
		{/if}
	</Background>

	{#if isHome}
		<Footer/>
	{/if}
</div>
