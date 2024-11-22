<script>
	let serverAddress = $state('smp.deeka.me');
	let onlinePlayers = $state(0);
	let maxPlayers = $state(100);

	$effect(() => {
		// Simulating fetching server status
		setInterval(() => {
			onlinePlayers = Math.floor(Math.random() * maxPlayers);
		}, 5000);
	});
</script>

<div class="min-h-screen bg-gradient-to-b from-gray-900 via-purple-900 to-indigo-900 text-gray-200">
	<main class="container mx-auto px-4 py-8">
		<div class="mb-12 text-center">
			<h1 class="text-6xl font-bold">
				<span
					class="bg-gradient-to-r from-red-500 via-yellow-500 to-green-500 bg-clip-text text-transparent"
					>Dee</span
				><span
					class="bg-gradient-to-r from-green-500 via-blue-500 to-purple-500 bg-clip-text text-transparent"
					>ka MC</span
				>
			</h1>
			<p class="mb-8 text-xl text-gray-300 drop-shadow-md">
				A Minecraft server. Yeah a fucking minecraft server what else you want?
			</p>
			<div class="inline-block rounded-lg bg-gray-800/70 p-6 shadow-lg backdrop-blur-sm">
				<h3 class="mb-4 text-2xl font-semibold text-pink-400">Server Address</h3>
				<div class="flex items-center justify-center space-x-2">
					<input
						value={serverAddress}
						readonly
						class="rounded bg-gray-700 px-3 py-2 text-center font-mono text-gray-200"
					/>
					<button
						onclick={() => navigator.clipboard.writeText(serverAddress)}
						class="rounded bg-gray-700 px-4 py-2 text-gray-200 hover:bg-gray-600">Copy</button
					>
				</div>
				<p class="mt-4 text-gray-300">Players Online: {onlinePlayers}/{maxPlayers}</p>
			</div>
		</div>

		<div class="grid gap-8 md:grid-cols-2">
			<div class="rounded-lg bg-gray-800/70 p-6 shadow-lg backdrop-blur-sm">
				<h3 class="mb-4 text-2xl font-semibold text-pink-400">Server Rules</h3>
				<ul class="list-inside list-disc space-y-2 text-gray-300">
					<li>Respect everyone</li>
					<li>No hate speech, discrimination, or offensive language</li>
					<li>No griefing or stealing from other players</li>
					<li>No cheating, hacking, or using unfair advantages</li>
				</ul>
			</div>
			<div class="rounded-lg bg-gray-800/70 p-6 shadow-lg backdrop-blur-sm">
				<h3 class="mb-4 text-2xl font-semibold text-pink-400">What We Have</h3>
				<ul class="list-inside list-disc space-y-2 text-gray-300">
					<li>Good admin</li>
					<li>Custom pronous in SMP</li>
					<li>We support LGBTQIANTANKATTACKHELICOPTERAATANKANTIAIRCRAFT</li>
				</ul>
			</div>
		</div>
	</main>

	<footer class="mt-8 bg-gray-800/70 py-4 backdrop-blur-sm">
		<div class="container mx-auto px-4 text-center">
			<div class="space-x-4">
				<button class="text-gray-300 hover:text-gray-100">Discord</button>
				<button class="text-gray-300 hover:text-gray-100">Blog</button>
			</div>
		</div>
	</footer>
</div>
