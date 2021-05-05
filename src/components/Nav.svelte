<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	/* ul {
		margin: 0;
		padding: 0;
	} */

	/* clearfix */
	/* ul::after {
		content: '';
		display: block;
		clear: both;
	} */

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
	.navbar-item img {
		max-height: 100%;
	}
</style>

<!-- <nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === 'heros' ? 'page' : undefined}" href="heros">Champions</a></li>
		<li><a aria-current="{segment === 'news' ? 'page' : undefined}" href="news">News</a></li>
		<li><a aria-current="{segment === 'items' ? 'page' : undefined}" href="items">Items</a></li>
		<li><a aria-current="{segment === 'spells' ? 'page' : undefined}" href="spells">Spells</a></li>
		<li><a aria-current="{segment === 'emblems' ? 'page' : undefined}" href="emblems">Emblems</a></li> -->

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li> -->
	<!-- </ul>
</nav> -->

<nav class="navbar" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
	  <a class="navbar-item" href="/">
		<img src="logo-company.png" width="300" height="190" alt="logo">
	  </a>
  
	  <div role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
		<span aria-hidden="true"></span>
		<span aria-hidden="true"></span>
		<span aria-hidden="true"></span>
	  </div>
	</div>
  
	<div id="navbarBasicExample" class="navbar-menu">
	    <div class="navbar-end">
		<div class="navbar-item">
			<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
			<li><a aria-current="{segment === 'champions' ? 'page' : undefined}" href="champions">Champions</a></li>
			<li><a aria-current="{segment === 'news' ? 'page' : undefined}" href="news">News</a></li>
			<li><a aria-current="{segment === 'items' ? 'page' : undefined}" href="items">Items</a></li>
			<li><a aria-current="{segment === 'spells' ? 'page' : undefined}" href="spells">Spells</a></li>
			<li><a aria-current="{segment === 'emblems' ? 'page' : undefined}" href="emblems">Emblems</a></li>
		</div>
	  </div>
	</div>
  </nav>