<script>
	export let data = '';
</script>

<div class="card mt-5 variant-soft p-4">
	{#each Object.entries(JSON.parse(data)) as [key, value]}
		<div class="ml-2">
			<p class="h4"><span class="font-bold capitalize">{key.replace('_', ' ')}</span> = {value}</p>
		</div>
	{/each}
</div>
