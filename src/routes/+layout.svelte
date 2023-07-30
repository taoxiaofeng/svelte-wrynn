
<script lang="ts">
	import { fns, AppShell, Navbar, Header, Title, Divider } from '@svelteuidev/core';
	import HeadContent from '../components/HeadContent.svelte';
	import NavContent from '../components/NavContent.svelte';

	let isDark = false;
	let opened = false;

	function toggleTheme() {
		isDark = !isDark;
	}
	function toggleOpened() {
		opened = !opened;
	}
</script>

<AppShell>
	<Navbar slot="navbar" hidden={!opened}>
		<NavContent />
	</Navbar>
	<Header slot="header">
		<HeadContent />
	</Header>

	<slot>This is the main content</slot>
</AppShell>