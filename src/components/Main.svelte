<script>
    	const scroll = async (e) => {
		const div = e.target

        x =Math.round(((div.scrollTop  - (div.scrollHeight - div.clientHeight))/ (div.scrollHeight - div.clientHeight)*-1)*100)
	}
    let x = 100
</script>

<div on:scroll={scroll} class="overflow-y-auto backdrop-blur-md z-40 lg:grow h-[90vh] lg:h-screen w-screen">
    <slot />
</div>
