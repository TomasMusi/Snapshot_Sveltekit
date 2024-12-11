<script lang="ts">
	import type { Snapshot } from './$types';

	let information = $state<{
		name: string;
		phone: string;
		email: string;
		password: string;
	}>({
		name: '',
		phone: '',
		email: '',
		password: ''
	});

	export const snapshot: Snapshot = {
		capture: () => information,
		restore: (value) => (information = value)
	};
</script>

<section class="h-full bg-[#2e3440] p-80">
	<h1 class="items-center text-center text-4xl text-white">Testing Snapshot Library</h1>

	<div class="m-auto flex w-1/2 flex-col justify-center p-7">
		<input
			class="m-auto mt-3 w-1/2 rounded-md border-2 border-white bg-transparent p-2 font-bold text-white"
			type="text"
			bind:value={information.name}
			placeholder="Enter Your Name"
		/>
		<input
			class="m-auto mt-3 w-1/2 rounded-md border-2 border-white bg-transparent p-2 font-bold text-white"
			type="tel"
			bind:value={information.phone}
			placeholder="Enter Your Phone Number"
		/>
		<input
			class="m-auto mt-3 w-1/2 rounded-md border-2 border-white bg-transparent p-2 font-bold text-white"
			bind:value={information.email}
			type="email"
			placeholder="Enter Your Email"
		/>
		<input
			class="m-auto mt-3 w-1/2 rounded-md border-2 border-white bg-transparent p-2 font-bold text-white"
			bind:value={information.password}
			type="password"
			placeholder="Enter Your Password"
		/>
		<button
			class="m-auto mt-3 w-1/4 justify-center rounded-md bg-blue-600 p-4 text-white"
			type="submit">Submit</button
		>
		<a
			class="m-auto justify-center text-blue-500 hover:underline hover:decoration-2 hover:transition-all hover:duration-300"
			href="/bla">Blabla</a
		>
	</div>
</section>
