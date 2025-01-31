<script lang="ts">
	let { close } = $props();
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div onclick={close} class="contents">
	<div id="links" class="allcenter space-x-8 min-[780px]:mr-8 font-medium">
		<a href="https://swap.choc.cy/pools" class=""> Pools </a>
	</div>
	<a href="https://swap.choc.cy/" class="clickable pinkpill py-2 px-7 font-semibold"> Swap Now </a>
</div>

<style lang="less">
	.pinkpill {
		border: 2.5px solid var(--mulberry);
		&:hover {
			border: 2.5px solid var(--pink);
		}
	}
</style>
