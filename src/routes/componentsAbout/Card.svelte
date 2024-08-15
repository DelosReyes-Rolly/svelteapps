<script lang="ts">
	import { Card } from 'flowbite-svelte';
</script>

<main>
	<Card style="margin: 8em auto 0;" size="xl">
		<div>
			<div class="title">Svelte Weather App</div>
			<br />
			<a href="https://github.com/DelosReyes-Rolly/svelteweatherapp" class="link">GitHub Link</a><br
			/>
			<span class="subtitle">Tech Stack: </span>
			<span class="tech-description">&nbsp; Svelte Kit, Svelte Material UI, OpenWeatherMap API</span
			><br />
			<span class="subtitle">Description: </span>
			<span class="tech-description">
				&nbsp; Completed an online weather app using svelte that shows the current temperature,
				humidity and wind speed of certain places. It also includes the forecast for the next days.
			</span>

			<br /><br /><br /><br />

			<div class="title">Svelte To do List</div>
			<br />
			<a href="https://github.com/DelosReyes-Rolly/sveltetodo" class="link">GitHub Link</a><br />
			<span class="subtitle">Tech Stack:</span>
			<span class="tech-description">&nbsp; Svelte Kit, Tailwind CSS, Flow bite Svelte</span><br />
			<span class="subtitle">Description: </span>
			<span class="tech-description">
				&nbsp; Constructed an online to do list that includes CRUD operations (create, read, update,
				and delete).
			</span>
		</div>
	</Card>
</main>

<style>
	.title {
		font-size: 28px;
		color: black;
		font-weight: bold;
	}

	.subtitle {
		font-size: 20px;
		color: black;
		font-weight: bold;
		display: inline-block;
	}

	.link {
		font-size: 20px;
		color: blue;
	}

	.link:hover {
		text-decoration: underline;
	}

	.tech-description {
		font-size: 20px;
		color: black;
	}
</style>