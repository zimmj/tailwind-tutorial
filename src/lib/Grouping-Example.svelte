<script>
	import Button from './Button.svelte';
</script>

<div class="p-2">
	Styling by group allows to change the style of a group of elements when hovering over the parent
	element.
</div>

<di class="flex">
	<div class="group w-full border hover:bg-sky-500">
		<div class="p-4">
			<h1 class="text-2xl font-bold group-hover:text-white">Group</h1>
			<p class="text-gray-500 group-hover:text-white">Change text color on group hover</p>
		</div>
	</div>
</di>

<div class="p-2">Styling by peer allows to listen to state changes of a peer element.</div>

<form class="p-4">
	<label class="flex w-full flex-col">
		<span class="block pb-1 pl-3 text-sm font-medium text-slate-700">Email</span>
		<input type="email" class="peer rounded-full border-2" />
		<p class="invisible mt-2 text-sm text-pink-600 peer-invalid:visible">
			Please provide a valid email address.
		</p>
	</label>
</form>

<div class="p-2">
	Styling by descandet allows to react on a change of the child, like a checkbox.
</div>

<div class="flex items-center justify-center">
	<label
		class="flex items-center rounded-md border-2 p-4 has-[:checked]:border-transparent has-[:checked]:bg-indigo-50 has-[:checked]:text-indigo-900 has-[:checked]:ring-indigo-200"
	>
		<p class="pr-4">Check me to see the changes</p>
		<input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600" />
	</label>
</div>
