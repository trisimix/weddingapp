<script>
	import Confet from "./Confet.svelte"
	import Svg from "./Svg.svelte"
	import { Button, MaterialApp } from 'svelte-materialify';
</script>
<Confet ></Confet>

<title> Josh and Sarah's wedding</title>
<main>
	
	<p><span>Save</span></p>
	<p><span>the</span></p>
	<p><span>date</span>
	<span>.</span></p>
	<p><span1>July</span1> <span1>2</span1><span3 style="position:relative;top:-1em;opacity:1">nd</span3> <span1>2022</span1></p>
	<p><Button fab size="large" class="red white-text rounded">RSVP</Button></p>
	<Button>Can't make it</Button>
</main>

<style>
	
	@font-face {
  font-family: 'Open Sans';
  font-style: normal;
  font-weight: 400;
  src: local('Open Sans'), local('OpenSans'), url('http://themes.googleusercontent.com/static/fonts/opensans/v5/cJZKeOuBrn4kERxqtaUH3T8E0i7KZn-EPnyo3HZu7kw.woff') format('woff');
}
	main {
		position: relative;
		width: 100%;
		height: 100%;
		overflow: hidden;
		text-align: left;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		font-family: Inter,Bahnschrift,-apple-system,BlinkMacSystemFont,Helvetica Neue,sans-serif;
	}
	span {
		color: #2b2b2b;
		font-size: 5.5em;
		letter-spacing: -.08em;
		font-weight: 500;
		display: inline-block;
		transform: none;
	}
	span1{
		font-family: 'open sans',arial,sans-serif;
		font-size: 4em;
	}
	span3{
		font-size: 2em;
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