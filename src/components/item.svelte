<svelte:head>
	<title>Sapper project template</title>
</svelte:head>
<script>
    export let item;
</script>

<table>
    <tbody>
        <tr>
          <td><figure class="image is-128x128">
            <img src="{item.icon}" aria-hidden="true" class="is-rounded itemicon" alt="item picture" /> 
            </figure></td>
          <td><h1 class="itemname">{item.name}</h1></td>
        </tr>
    </tbody>
  </table>

  <style>
    .itemname {
      font-size: 1.1rem ;
      font-weight: 700 ;
      margin-top: 15%;
    }
    .itemicon {
      width: 60%;
    }
  </style>