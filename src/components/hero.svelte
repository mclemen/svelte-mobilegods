<svelte:head>
	<title>Sapper project template</title>
</svelte:head>
<script>
    export let hero;
</script>
  
  <table>
    <tbody>
        <tr>
          <td>
            <figure class="image is-128x128">
            <img src="{hero.key}" aria-hidden="true" class="is-rounded heropic" alt="cover picture" /> 
            </figure>
          </td>
          <td><h1 class="heroname">{hero.name}</h1>
            <button class="button is-info" data-target = "#modal">Show</button>
          </td>
        </tr>
    </tbody>
  </table>

  <div class="modal">
    <div class="modal-background"></div>
    <div class="modal-card">
      <header class="modal-card-head">
        <p class="modal-card-title">Modal title</p>
        <button class="delete" aria-label="close"></button>
      </header>
      <section class="modal-card-body">
        <!-- Content ... -->
      </section>
      <footer class="modal-card-foot">
        <button class="button is-success">Save changes</button>
        <button class="button">Cancel</button>
      </footer>
    </div>
  </div>


  <style>
    .heroname {
      font-size: 1.1rem ;
      font-weight: 700 ;
      margin-top: 20%;
    }
    .heropic {
      width: 70%;
    }
  </style>