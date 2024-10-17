<script lang="ts">
	import DialogModal from '$lib/components/DialogModal.svelte';

	let modals = $state(0);
</script>

<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<DialogModal isOpen={true}>
	<div class="content">
		<h1>Dialog Modal</h1>
		<p>This is a dialog modal</p>
	</div>
</DialogModal>

<DialogModal isOpen={true}>
	<div class="content">
		<h1>That's a big dialog Modal</h1>
		<h2>That's a big dialog Modal</h2>
		<p>
			There is so much content in here it's crazy! Lorem ipsum dolor sit amet, consectetur
			adipiscing elit. Aliquam at porttitor sem. Aliquam erat volutpat.
		</p>

		<button
			onclick={() => {
				modals++;
			}}>Open a stacked one!</button
		>
	</div>
</DialogModal>

{#each { length: modals } as _, i}
	<DialogModal isOpen={true}>
		<div class="content">
			<h1>
				I'm stacked{'!'.repeat(i + 1)}
			</h1>
			<p>
				There is so much content in here it's crazy! Lorem ipsum dolor sit amet, consectetur
				adipiscing elit. Aliquam at porttitor sem. Aliquam erat volutpat.
			</p>

			<button
				onclick={() => {
					modals++;
				}}>And another one!</button
			>
		</div>
	</DialogModal>
{/each}

<style lang="scss">
	.content {
		background-color: yellowgreen;
		padding: 1rem;
		border-radius: 0.375rem;
	}
</style>
