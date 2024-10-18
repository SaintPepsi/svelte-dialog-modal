# Svelte Dialog Modal

An unstyled HTMLDialog Element wrapper for easy use in Svelte/SvelteKit, supporting stacking contexts and more.

<!-- get a StackBlitz badge: https://developer.stackblitz.com/guides/integration/open-from-github -->

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/edit/sveltejs-kit-template-default-qngg7x?file=src%2Froutes%2F%2Bpage.svelte)

## Features

- Simple integration with Svelte/SvelteKit
- Supports stacking contexts
- Unstyled for full customization

## Installation

```bash
bun add svelte-dialog-modal
```

## Usage

```svelte
<script lang="ts">
	import DialogModal from 'svelte-dialog-modal';
	let isOpen = $state(false);
</script>

<button onclick={() => (isOpen = true)}>Open Dialog</button>

<DialogModal bind:isOpen>
	<p>This is a dialog content.</p>
	<button onclick={() => (isOpen = false)}>Close</button>
</DialogModal>
```

## Props

- `isOpen` (`boolean`)- Indicates whether the modal is open.
- `children` (`Snippet`)- The content to be displayed inside the modal.
- `fullWidth` (`boolean`) - Optional. If true, the modal will take the full width of the screen.
- `noBackdrop` (`boolean`) - Optional. If true, the modal will not display a backdrop.
- `preventCloseOnOutsideClick` (`boolean`) - Optional. If true, clicking outside the modal will not close it.
- `type` (`'default' | 'popup'`) - Optional. Specifies the type of the modal. Can be 'default' or 'popup'.
- `'data-testid'` (`string`) - Optional. A test identifier for the modal.

## License

MIT License

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
