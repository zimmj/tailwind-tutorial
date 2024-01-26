<script lang="ts">
	import Button from '$lib/Button.svelte';
	import CardTailwind from '$lib/Card-Tailwind.svelte';
	import Card from '$lib/Card.svelte';
	import GroupingExample from '$lib/Grouping-Example.svelte';
	import SimpleList, { type User } from '$lib/SimpleList.svelte';

	let users: User[] = [
		{ name: 'John Doe', email: 'john@example.com' },
		{ name: 'Jane Smith', email: 'jane@example.com' },
		{ name: 'Bob Johnson', email: 'bob@example.com' }
	];
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

	<CardTailwind title="Simple List Showcases">
		<SimpleList {users} />
	</CardTailwind>

	<div class="invisible">
		<CardTailwind title="Grouping Showcase Parent">
			<GroupingExample />
		</CardTailwind>
	</div>
</div>
