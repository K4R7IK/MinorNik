<script>
	export let data = '';
	export let ModelName = '';
	import amdPic from '$lib/data/amd-icon.svg';
	import intelPic from '$lib/data/intel-icon.svg';
</script>

<div class="flex">
	<div class="flex flex-col items-center min-w-fit">
		<img
			src={ModelName.toLowerCase().includes('amd') ? amdPic : intelPic}
			alt="LOGO"
			class="max-w-lg m-auto"
		/>
		<h4 class="h4 text-center">{ModelName}</h4>
	</div>
	<div class="card variant-soft p-5 ml-20 w-full">
		{#each Object.entries(JSON.parse(data)) as [key, value]}
			<div class="ml-2">
				<p class="h4">
					<span class="font-bold capitalize">{key.replace('_', ' ')}</span> = {value}
				</p>
			</div>
		{/each}
	</div>
</div>
