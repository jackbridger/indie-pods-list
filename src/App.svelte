<script lang="ts">
	export let name: string;
	import Pod from "./Pod.svelte";
	const pods = [{title:'Indie Bites', author:'James McKinven', url:'https://open.spotify.com/show/1MY9XdVViRwfaO8giM4fXO'},{title:'Indie Hackers', author:'Courtland Allen', url:'https://open.spotify.com/show/4ex8hmrHCPvPohKJb3wsuC'}]
</script>

<main>
	<h1>Indie Pods List</h1>
	<ul>
		{#each pods as pod}
			<li>
				<Pod title={pod.title}  author={pod.author} url={pod.url}  />
			</li>
		{/each}
	</ul>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>