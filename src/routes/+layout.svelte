<script>
	import Header from './Header.svelte';
	import './styles.css';

	export let email = 'haakongv@gmail.com';
	export let linkedin = 'https://www.linkedin.com/in/hakonveras/';
	export let github = 'https://github.com/hakver29';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<div class="footer-content">
			<div class="footer-contact">
				<p>Email: <a href="mailto:{email}">{email}</a></p>
				<p>LinkedIn: <a href="{linkedin}" target="_blank" rel="noopener noreferrer">LinkedIn</a></p>
				<p>GitHub: <a href="{github}" target="_blank" rel="noopener noreferrer">GitHub</a></p>
			</div>
		</div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		background-color: #333;
		color: #fff;
		padding: 20px 0;
	}

	.footer-content {
		display: flex;
		justify-content: center;
		align-items: center;
		max-width: 800px;
		margin: 0 auto;
		padding: 0 20px;
	}

	.footer-contact {
		text-align: center;
	}

	p {
		margin: 5px 0;
	}

	a {
		color: #fff;
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
