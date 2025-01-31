<script lang="ts">
	import Background from '$lib/components/common/background.svelte';
	import '@fontsource/roboto';
	import '../app.less';
	import Footer from '$lib/components/home/footer.svelte';
	import Header from '$lib/components/common/header.svelte';
	let { children } = $props();
</script>

<div class="overflow-hidden relative bg-black min-h-screen flex flex-col justify-between">
	<Header />

	<Background>
		{@render children()}
	</Background>

	<Footer/>
</div>
