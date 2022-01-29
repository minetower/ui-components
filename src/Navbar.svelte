<script>
	export let title = '',
		repo_url = '',
		center_title = false
</script>

<nav class="relative w-full flex flex-wrap justify-between py-3 bg-slate-300">
	<div
		class="collapse navbar-collapse container-fluid w-full flex flex-wrap items-center justify-between px-6">
		<img class="w-6" src="/assets/images/logo.png" alt="logo" />
		<div class="items-center md:mt-1" class:flex-grow={!center_title}>
			<a
				class="hidden sm:inline text-gray-100 text-xs md:text-base logo"
				class:pl-5={!center_title}
				href="/">
				{title}
			</a>
		</div>
		<div class="flex items-center">
			<div class="bg-white rounded-sm p-px">
				<a
					class="opacity-70 hover:opacity-80 focus:opacity-80"
					href="//github.com/minetower{repo_url}">
					<img src="/assets/images/github-square.svg" alt="github" />
				</a>
			</div>
		</div>
	</div>
</nav>

<style>
	@font-face {
		font-family: 'PressStart2P';
		src: url('/assets/fonts/PressStart2P/PressStart2P-Regular.ttf');
	}
	nav {
		font-family: 'PressStart2P';
		background: url(/assets/images/grass-top.png) repeat-x;
		background-size: 12em 100%;
	}
	.logo {
		text-shadow: -2px 3px 3px black;
	}
</style>
