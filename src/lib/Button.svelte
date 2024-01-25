<script lang="ts">
	let count = 0;

	function handleClick() {
		count++;
		if (count % 7 === 0) {
			console.log(count);
		}
	}
</script>

<button
	class="bg-green-500 hover:bg-green-600 focus:outline-none focus:ring focus:ring-green-300 active:bg-green-700"
	on:click={handleClick}>Click me</button
>
