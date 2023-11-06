<script>
	import { filtered } from '$lib/data/Data.json';
	import Info from './bios/info.svelte';
	import Details from './bios/details.svelte';
  let system = filtered.system;
  let BIOS = filtered.BIOS;
</script>

<div class="card p-4 m-8 rounded-lg">
	<Info imgText={system.manufacturer} data={JSON.stringify(system)} logoType={system.manufacturer} />
	<Details data={JSON.stringify(BIOS)} />
</div>
