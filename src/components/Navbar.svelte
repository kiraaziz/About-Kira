<script>

    let routes = [
		{ name: 'Kira', url: '/#Kira', icon: 'rout/kira' },
		{ name: 'Stack', url: '/#Stack', icon: 'rout/stack' },
		{ name: 'Projects', url: '/#Projects', icon: 'rout/projects' },
		{ name: 'Contact', url: '/#Contact', icon: 'rout/contact' },
		]

</script>

	<div
		class="z-30 lg:h-screen lg:w-96 w-screen h-24 lg:bg-primary bg-primary-focus/70 flex items-center justify-center lg:flex-col flex-row lg:space-y-3 space-x-2"
	>
		{#each routes as route}
	
			<a class="lg:w-11/12 h-[10vh] w-20  hover:font-bold font-medium rounded-lg lg:bg-primary-focus/60 hover:bg-primary-focus transition ease-in-out duration-200 hover:-translate-y-1 hover:shadow-xl flex lg:justify-start items-center justify-center lg:flex-row lg:pl-6 lg:space-x-5" href={route.url} >
				<img class=" h-10 w-10" src={`/icons/${route.icon}.svg`} alt={route.name} />
				<h1 class={`lg:block hidden  text-white  text-xl`}>{route.name}</h1>
			</a>
		{/each}
	</div>
