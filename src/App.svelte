<script>
	import { Router, Link, Route } from 'svelte-routing';
	import Home from './routes/Home.svelte';
	import About from './routes/About.svelte';
	export let url = '';
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" />
</svelte:head>

<Router {url}>
	<nav>
		<Link to="/">Home</Link>
		<Link to="about">About</Link>
	</nav>
	<div>
		<Route path="about" component={About} />
		<Route path="/" component={Home} />
	</div>
</Router>
