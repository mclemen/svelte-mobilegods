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
          <td>
            <div class="wrapper">
              <h1 class="heroname">{hero.name}</h1>
              
            </div>
          </td>
          <td>
            <div class="wrapper">
		          <div class="box icon-gear">
                <b class="tooltip"><img class="heroskill" src="{hero.skill["skill"][0]["icon"]}" alt="Hero Skill" />
                <span><p>{hero.skill["skill"][0]["des"]}</p></span></b>
                <b class="tooltip"><img class="heroskill" src="{hero.skill["skill"][1]["icon"]}" alt="Hero Skill" />
                <span><p>{hero.skill["skill"][1]["des"]}</p></span></b>
                <b class="tooltip"><img class="heroskill" src="{hero.skill["skill"][2]["icon"]}" alt="Hero Skill" />
                <span><p>{hero.skill["skill"][2]["des"]}</p></span></b>
                <b class="tooltip"><img class="heroskill" src="{hero.skill["skill"][3]["icon"]}" alt="Hero Skill" />
                <span><p>{hero.skill["skill"][3]["des"]}</p></span></b>
              </div>    
            </div>
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
      color: #fff;
    }
    .heropic {
      width: 70%;
    }
    .heroskill {
      width: 20%;
    }
    .wrapper{
position: relative;
margin-left: 15%;
}

.tooltip:hover span {
opacity: 1;
/* filter: alpha(opacity=100); */
top: -6em;
left: 20em;
z-index: 99;
-webkit-transition: all 0.2s ease;
-moz-transition: all 0.2s ease;
-o-transition: all 0.2s ease;
transition: all 0.2s ease;
}

.box b {
  color: #fff;
  box-shadow: none;
}

.tooltip span {
	background: none repeat scroll 0 0 #222; /*-- some basic styling */
	color: #F0B015;
	font-family: 'Helvetica';
	font-size: 0.8em;
	font-weight: normal;
	line-height: 1.5em;
	padding: 16px 15px;
	width: 300px;
	top: 0;  /*-- this is the original position of the tooltip when it's hidden */
	/* left: 50%; */
	margin-left: 0;	
	/*-- set opacity to 0 otherwise our animations won't work */
	opacity: 0;
	/* filter: alpha(opacity=0);  	 */
	position: absolute;
	text-align: center;	
	z-index: 1;
	text-transform: none;
	-webkit-transition: all 0.3s ease;
	-moz-transition: all 0.3s ease-in-out;
	-o-transition: all 0.3s ease;
	transition: all 0.3s ease-in-out;
}

.tooltip span:after {
	border-color: #222 rgba(0, 0, 0, 0);
	border-style: solid;
	border-width: 15px 15px 0;
	bottom: -15px;
	content: "";
	display: block;
	/* left: 31px; */
	position: absolute;
	width: 0;
  /* top: 100%;
  left: 50%; */
  margin-left: -5px;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
    margin: 0 auto;
    width: 100%;
}

.icon-gear {
  background-color: transparent;
}

</style>