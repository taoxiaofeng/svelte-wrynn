
<script lang="ts">
	import { Footer, AppShell, Navbar, Header, Aside, ShellSection } from '@svelteuidev/core';
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
	<Navbar
		width={{
			// When viewport is larger than theme.breakpoints.sm, Navbar width will be 45px
			sm: 45,

			// When viewport is larger than theme.breakpoints.lg, Navbar width will be 240px
			lg: 240,

			// When other breakpoints do not match base width is used, defaults to 100%
			base: 240
		}}
	>
		<!-- First section with normal height (depends on section content) -->
		<ShellSection grow>First section</ShellSection>
	</Navbar>
	<!-- <Header fixed slot="header">
		<HeadContent />
	</Header> -->
	<slot>This is the main content</slot>
</AppShell>