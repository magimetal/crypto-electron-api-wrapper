<script>
	import Dashboard from './routes/Dashboard.svelte';
	import Settings from './routes/Settings.svelte';
	import Header from "./components/Header.svelte";

	let localState = 'Dashboard';
</script>

<style>
	#wrapper {
		padding: 56px 8px 8px;
	}
</style>

<div id="wrapper">
	<Header bind:name="{localState}"/>
	{#if localState === 'Dashboard'}
		<Dashboard/>
	{:else if localState === 'Settings'}
		<Settings/>
	{/if}
</div>