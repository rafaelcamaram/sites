<script>
	import '@sveltejs/site-kit/base.css';
	import { page } from '$app/stores';
	import { Icons, Icon, Nav, NavItem } from '@sveltejs/site-kit';

	// TODO
	export let segment;
</script>

<style>
	/* :global(html) {
		--prime: rgb(21, 151, 148) !important;
	} */

	main {
		position: relative;
		margin: 0 auto;
		/* padding: var(--nav-h) var(--side-nav) 0 var(--side-nav); */
		padding: var(--nav-h) 0 0 0;
		overflow-x: hidden;
	}
</style>

<Icons/>

<Nav {segment} {page} logo="images/svelte-kit-horizontal.svg">
	<NavItem segment="docs">Docs</NavItem>
	<NavItem segment="migrating">Migrating</NavItem>

	<NavItem external="https://svelte.dev">Svelte</NavItem>

	<NavItem external="https://svelte.dev/chat" title="Discord Chat">
		<Icon name="message-square"/>
	</NavItem>

	<NavItem external="https://github.com/sveltejs/kit" title="GitHub Repo">
		<Icon name="github"/>
	</NavItem>
</Nav>

<main>
	<slot></slot>
</main>
