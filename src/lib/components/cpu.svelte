<script>
	import { filtered } from '$lib/data/Data.json';
	import Info from './cpu/info.svelte';
	import Details from './cpu/details.svelte';
  let cpu = filtered.cpu;
</script>

<div class="card p-4 m-8 rounded-lg">
	<Info data={JSON.stringify(cpu.About)} ModelName={cpu.Model_name} />
	<Details data={JSON.stringify(cpu)} />
</div>
