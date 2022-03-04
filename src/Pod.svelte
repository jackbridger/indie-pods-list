<script lang="ts">
    export let title: string;
    export let author: string;
    export let url: string;
</script>

<main>
	<h2>{title}</h2>
    <h3>A pod by {author}</h3>
	<p>Listen <a href={url}>here</a></p>
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