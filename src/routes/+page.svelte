<script>
	import Button from '$lib/Button.svelte';
	import CardTailwind from '$lib/Card-Tailwind.svelte';
	import Card from '$lib/Card.svelte';
</script>

<div>
	<Card title="Tailwind Tutorial">
		<div>
			<p>This is a simple tutorial, don't expect to much</p>
		</div>
		<div>
			<p>But after you should have learned some basic css.</p>
			<p>And how to use <b>Tailwind</b> combiened with your knowledge of css.</p>
			<p><b>Tailwind</b> does not <mark>remove</mark> the requirement, that you know css.</p>
		</div>
	</Card>

	<CardTailwind title="Tailwind Tutorial">
		<div>
			<p>This is a simple tutorial, don't expect to much</p>
		</div>
		<div>
			<p>But after you should have learned some basic css.</p>
			<p>And how to use <b>Tailwind</b> combiened with your knowledge of css.</p>
			<p><b>Tailwind</b> does not <mark>remove</mark> the requirement, that you know css.</p>
		</div>
		<Button />
	</CardTailwind>
</div>
