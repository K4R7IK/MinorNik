<script>
	import asusPic from '$lib/data/ASUS_Logo.svg';
  import lenovoPic from '$lib/data/lenovo-2.svg';
	export let imgText = '';
	export let data = '';
  export let logoType = '';
</script>

<div class="flex">
	<div class="flex flex-col items-center min-w-fit">
		<img src={logoType.toLowerCase().includes('asus') ? asusPic : lenovoPic} alt="LOGO" class="max-w-lg m-auto" />
		<h4 class="h4 text-center">{imgText}</h4>
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
