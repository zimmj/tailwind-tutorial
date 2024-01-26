<script context="module" lang="ts">
	export interface User {
		name: string;
		email: string;
	}
</script>

<script lang="ts">
	export let users: User[] = [];
</script>

<ul role="list" class="divide-y divide-slate-200 border p-6">
	{#each users as user}
		<li class="flex py-4 first:pt-0 last:pb-0">
			<div class="ml-3 overflow-hidden">
				<p class="truncate text-sm font-medium text-slate-500">{user.name}</p>
				<p class="truncate text-sm text-slate-500">{user.email}</p>
			</div>
		</li>
	{/each}
</ul>
