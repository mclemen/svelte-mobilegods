<svelte:head>
	<title>Items</title>
</svelte:head>

<script>
    import { onMount } from "svelte";
    import Item from "../components/item.svelte";
    let items;

    onMount(async () => {
    await fetch(`http://localhost:8081/items`)
      .then(r => r.json())
      .then(data => {
        items = data;
      });
  })

</script>

{#if items}
  <table>
	<tbody>
		{#each items as item}
			<tr>
				<td><Item {item} /></td>
			</tr>
		{/each}
	</tbody>
</table>

{:else}
  <p class="loading">loading...</p>
{/if}