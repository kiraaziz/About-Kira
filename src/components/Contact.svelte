<script>

	let name
	let email
	let message
	let code
	let i

	const Send  =async()=>{

		const sendMessage = await fetch('https://stale-camera.pockethost.io/api/collections/fireBlogMessages/records', {
			method: 'POST',
			headers: {
			'Accept': 'application/json',
			'Content-Type': 'application/json'
			},
			body: JSON.stringify({
				name: name,
				email: email,
				message: message
			})
		})

		const result = await sendMessage.json()

		code = result.code
		i = "Done"
		
	}
</script>
<h1 class="mt-10 text-white text-4xl font-bold shadow-xl px-3 py-1 text-white bg-gradient-to-tr from-blue-600 to-red-600 w-max mx-auto">My Stack</h1>

<div id="Contact" class="grid bg-gray-900 max-w-screen-xl grid-cols-1 gap-8 px-8 py-16 mx-auto rounded-lg md:grid-cols-2 md:px-12 lg:px-16 xl:px-32 ">
	<div class="flex flex-col justify-between">
		<div class="space-y-2">
			<h2 class="text-4xl font-bold leading-tight lg:text-5xl">Let's talk!</h2>
			<div class="dark:text-gray-400">Tell me what you want</div>
		</div>
		<img src="/images/show2.gif" alt="" class="p-6 h-80 rounded-lg object-cover">
	</div>
	<div class="space-y-6 ng-untouched ng-pristine ng-valid">
		<div>
			<label for="name" class="text-sm">Full name</label>
			<input bind:value={name} id="name" type="text" placeholder="Kira Aziz" class="w-full p-3 rounded bg-gray-800 border-2">
		</div>
		<div>
			<label for="email" class="text-sm">Email</label>
			<input bind:value={email} id="email" type="email" placeholder="kira12@exemple.com" class="w-full border-2 p-3 rounded bg-gray-800">
		</div>
		<div>
			<label for="message" class="text-sm">Message</label>
			<textarea bind:value={message} id="message" rows="3" placeholder="Hello over there" class="w-full border-2 p-3 rounded bg-gray-800"></textarea>
		</div>
		<button class="w-full p-3 text-sm font-bold tracking-wide uppercase rounded bg-primary">Send Message</button>
	</div>
	<div>
		{#if i && !code }
			<div class="w-full px-4 py-2 font-bold rounded shadow focus:outline-none f4 text-white bg-green-500 text-center">Message Sended Go To Home Page</div>
		{/if}
		{#if code}
			<div class="w-full px-4 py-2 font-bold rounded shadow focus:outline-none f4 text-white bg-red-500 text-center">Some Thing Is Wrong Try Again</div>
		{/if}
	</div>
</div>
