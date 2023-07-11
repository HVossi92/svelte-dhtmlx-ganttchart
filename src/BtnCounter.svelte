<svelte:options tag="btn-counter"/>
<script>
	import {onMount} from "svelte";
	export let count = 0;

	function increment(){
		count++;
	}
	function reset(){
		count = 0;
	}
	onMount(()=>{
		console.log("Btn has beend mounted");
	})
</script>

<style>
	button {
		width: 100px;
		height: 100px;
	}
</style>

<h2>BtnCounter.svelte</h2>

<button on:click={increment}> Count {count} </button>
<button on:click={reset}> Reset </button>