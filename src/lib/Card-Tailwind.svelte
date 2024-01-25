<script lang="ts">
	export let title: string;
</script>

<div class="flex justify-center">
	<div class="m-6 rounded-lg border border-solid border-gray-300 p-4">
		<div class="border-b border-solid border-gray-300">
			<h2 class="text-3xl">{title}</h2>
		</div>
		<div class="my-6">
			<slot />
		</div>
	</div>
</div>
