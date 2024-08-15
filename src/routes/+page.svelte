<script>
	import Main from './main/Main.svelte';
</script>

<svelte:head>
	<title>Svelte</title>
	<meta name="description" content="Svelte Todo List App" />
	<!-- Fonts -->
	<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons" />
	<link
		rel="stylesheet"
		href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,600,700"
	/>

	<!-- Material Typography -->
	<link
		rel="stylesheet"
		href="https://unpkg.com/@material/typography@14.0.0/dist/mdc.typography.css"
	/>

	<!-- SMUI -->
	<link rel="stylesheet" href="https://unpkg.com/svelte-material-ui/bare.css" />
</svelte:head>
<Main />