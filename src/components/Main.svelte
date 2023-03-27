<script>
    	const scroll = async (e) => {
		const div = e.target

        x =Math.round(((div.scrollTop  - (div.scrollHeight - div.clientHeight))/ (div.scrollHeight - div.clientHeight)*-1)*100)
	}
    let x = 100
</script>

<div class=" z-20 h-full w-full overflow-hidden absolute top-0 right-0  ">
    <div class="bg-primary h-max transition ease-in-out duration-200 m-auto" style={`scale: ${1- x/100}`}>x</div>
</div>
<div on:scroll={scroll} class="overflow-y-auto backdrop-blur-md z-40 grow h-[90vh] lg:h-screen w-screen">
    <slot />
</div>
