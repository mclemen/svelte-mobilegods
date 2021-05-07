<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<script>
    import { onMount } from "svelte";
    import Hero from "../components/hero.svelte";
    let heros;

    onMount(async () => {
    await fetch(`http://localhost:8081/heros`)
      .then(r => r.json())
      .then(data => {
        heros = data;
      });
  })

</script>

{#if heros}
  <table>
	<tbody>
		{#each heros as hero}
			<tr>
				<td><Hero {hero} /></td>
			</tr>
		{/each}
	</tbody>
</table>

{:else}
  <p class="loading">loading...</p>
{/if}