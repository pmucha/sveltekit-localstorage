<script lang="ts">
	import { data } from '../stores/index';

	let inputValue = $data ?? '';

	function saveData() {
		$data = inputValue;
	}
</script>

<h1>SvelteKit localStore: about</h1>
<p>
	Current data: {$data}
</p>
<p>
	<input bind:value={inputValue} placeholder="New store value..." />
	<button on:click={saveData}>Save to store</button>
</p>
