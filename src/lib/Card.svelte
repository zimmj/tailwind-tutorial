<script lang="ts">
	export let title: string;
</script>

<div class="holder">
	<div class="card">
		<div class="card-header">
			<h2>{title}</h2>
		</div>
		<div class="card-body">
			<slot />
		</div>
	</div>
</div>

<style>
	.holder {
		display: flex;
		justify-content: center;
	}
	h2 {
		font-size: 32px;
	}
	.card {
		border: 1px solid #ccc;
		border-radius: 15px;
		margin: 24px;
		padding: 16px;
	}
	.card-header {
		border-bottom: 1px solid #ccc;
	}
	.card-body {
		margin: 24px 0;
	}
</style>
