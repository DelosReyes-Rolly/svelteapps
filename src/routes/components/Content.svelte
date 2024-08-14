<script>
	import MainTodo from '../mainTodo/MainTodo.svelte';
	import MainWeather from '../componentsWeather/MainWeather.svelte';
	import { InfoCircleOutline, NewspaperOutline, SunOutline } from 'flowbite-svelte-icons';
	import MainAbout from '../componentsAbout/MainAbout.svelte';
</script>

<main>
	<div class="layout">
		<input name="nav" type="radio" class="nav home-radio" id="home" checked />
		<div class="page home-page todo-bg bg">
			<MainTodo />
		</div>
		<label class="nav" for="home">
			<span class="icon"><NewspaperOutline style="margin-top:-2px;" /></span>
			<b>&nbsp; TODO LIST APP</b>
		</label>

		<input name="nav" type="radio" class="about-radio" id="about" />
		<div class="page about-page weather-bg bg">
			<MainWeather />
		</div>
		<label class="nav" for="about">
			<span class="icon"><SunOutline style="margin-top:-2px;" /></span>
			<b>&nbsp; WEATHER APP</b>
		</label>

		<input name="nav" type="radio" class="contact-radio" id="contact" />
		<div class="page contact-page weather-bg bg">
			<MainAbout />
		</div>
		<label class="nav" for="contact">
			<span class="icon"><InfoCircleOutline style="margin-top:-2px;" /></span>
			<b>&nbsp; ABOUT</b>
		</label>
	</div>
</main>

<style>
	* {
		font-family: 'Work Sans', sans-serif;
	}

	:global(body) {
		height: 100%;
		color: #1a1b1c;
	}

	label{
		cursor: pointer;
		user-select: none;
		text-decoration: none;
		display: inline-block;
		color: inherit;
		transition: border 0.2s;
		border-bottom: 5px solid rgba(142, 68, 173, 0.2);
		padding: 3px 2px;
	}
	label:hover{
		border-bottom-color: #9b59b6;
	}

	.layout {
		display: grid;
		height: 100%;
		width: 100%;
		overflow: hidden;
		grid-template-rows: 50px 1fr;
		grid-template-columns: 1fr 1fr 1fr;
	}

	input[type='radio'] {
		display: none;
	}

	label.nav {
		display: flex;
		align-items: center;
		justify-content: center;
		cursor: pointer;
		border-bottom: 2px solid #8e44ad;
		background: #ecf0f1;
		user-select: none;
		transition:
			background 0.4s,
			padding-left 0.2s;
		padding-left: 0;
	}
	input[type='radio']:checked + .page + label.nav {
		background: #9b59b6;
		color: #ffffff;
		padding-left: 20px;
	}
	input[type='radio']:checked + .page + label.nav span {
		padding-left: 20px;
	}
	input[type='radio']:checked + .page + label.nav svg {
		opacity: 1;
	}
	label.nav span {
		padding-left: 0px;
		position: relative;
	}
	label.nav svg {
		left: 0;
		top: -3px;
		position: absolute;
		width: 15px;
		opacity: 0;
		transition: opacity 0.2s;
	}

	.page {
		grid-column-start: 1;
		grid-row-start: 2;
		grid-column-end: span 3;
		padding: 0px 20px;
	}

	input[type='radio'] + .page {
		transition: transform 0.2s;
		transform: translateX(100%);
	}

	input[type='radio']:checked + .page {
		transform: translateX(0%);
	}
	input[type='radio']:checked {
		opacity: 1;
		transform: translateY(0px);
	}

	.todo-bg {
		background-image: url('todos-bg.jpg');
	}

	.weather-bg {
		background-image: url('bg.jpeg');
	}

	.bg {
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-size: 100% 100%;
		margin: 0;
		padding: 0;
	}
</style>
