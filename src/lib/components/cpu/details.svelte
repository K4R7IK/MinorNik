<script>
	export let data = '';
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
	import Subcard from '../subcard.svelte';
	import Icon from '@iconify/svelte';
</script>

<section class="mt-5">
	<Accordion autocollapse>
		<AccordionItem open>
			<svelte:fragment slot="lead">
				<Icon icon="solar:graph-up-bold" width="30" height="30" />
			</svelte:fragment>
			<svelte:fragment slot="summary">
				<h5 class="h5">Clock Speed</h5>
			</svelte:fragment>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).Scaling)} />
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead">
				<Icon icon="fluent:box-multiple-24-filled" width="28" height="28" />
			</svelte:fragment>
			<svelte:fragment slot="summary"
				><span class="font-semibold">Threads & Cache</span></svelte:fragment
			>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).Core)} />
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead">
				<Icon icon="solar:danger-bold" width="28" height="28" />
			</svelte:fragment>
			<svelte:fragment slot="summary"
				><span class="font-semibold">Vulnerability</span></svelte:fragment
			>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).Vulnerability)} />
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead">
				<Icon icon="material-symbols:emoji-flags" width="28" height="28" />
			</svelte:fragment>
			<svelte:fragment slot="summary"><span class="font-semibold">CPU Flags</span></svelte:fragment>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).flags)} />
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead">
				<Icon icon="mingcute:checkbox-fill" width="28" height="28" />
			</svelte:fragment>
			<svelte:fragment slot="summary"
				><span class="font-semibold">Characteristics</span></svelte:fragment
			>
			<svelte:fragment slot="content">
				<Subcard data={JSON.stringify(JSON.parse(data).characteristics)} />
			</svelte:fragment>
		</AccordionItem>
	</Accordion>
</section>
