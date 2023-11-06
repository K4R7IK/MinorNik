<script>
	import Cpu from '$lib/components/cpu.svelte';
	import Bios from '$lib/components/bios.svelte';
	import { browser } from '$app/environment';
	import Carousel from 'svelte-carousel';
	import { AppBar } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';

	let carousel;
	function goToCPU() {
		carousel.goTo(0);
	}
	function goToBIOS() {
		carousel.goTo(1);
	}
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
		<Icon icon="mdi:cpu-64-bit" width="30" height="30" />
	</svelte:fragment>
	<div class="btn-group variant-soft-surface">
		<button on:click={goToCPU}>CPU</button>
		<button on:click={goToBIOS}>BIOS</button>
	</div>
	<svelte:fragment slot="trail">
		<a href="https://www.github.com" target="_blank">
			<Icon icon="mdi:github" width="30" height="30" />
		</a>
	</svelte:fragment>
</AppBar>
{#if browser}
	<Carousel arrows={false} dots={false} bind:this={carousel}>
		<div><Cpu /></div>
		<div><Bios /></div>
	</Carousel>
{/if}
