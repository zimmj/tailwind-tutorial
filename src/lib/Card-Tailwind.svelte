<script lang="ts">
	export let title: string;
</script>

<div class="holder hidden">
	<div class="m-6 rounded-lg border border-gray-300 p-4">
		<div class="card-header">
			<h2>{title}</h2>
		</div>
		<div class="card-body">
			<slot />
		</div>
	</div>
</div>
