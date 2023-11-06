<script>
	export let data = '';
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';
	import Subcard from '../subcard.svelte';
</script>

<section class="mt-5">
	<Accordion autocollapse>
		<AccordionItem open>
			<svelte:fragment slot="lead">
				<Icon icon="material-symbols:memory-alt-rounded" width="30" height="30" />
			</svelte:fragment>
			<svelte:fragment slot="summary"><h5 class="h5">BIOS</h5></svelte:fragment>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).About)} />
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead">
				<Icon icon="ph:circuitry-fill" width="30" height="30" />
			</svelte:fragment>
			<svelte:fragment slot="summary"><h5 class="h5">BIOS Characteristics</h5></svelte:fragment>
			<svelte:fragment slot="content"
				>About
				<Subcard data={JSON.stringify(JSON.parse(data).characteristics)} />
			</svelte:fragment>
		</AccordionItem>
	</Accordion>
</section>
