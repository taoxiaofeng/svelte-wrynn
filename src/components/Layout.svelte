<!-- App.svelte -->

<script>
  import { fns, AppShell, Navbar, Header, Title, Divider } from '@svelteuidev/core';
  import HeadContent from '../components/HeadContent.svelte';
  import NavContent from '../components/NavContent.svelte';

  let isDark = false;
  let opened = false;

  function toggleTheme() {
    isDark = !isDark;
    document.body.classList.toggle('dark', isDark);
  }

  function toggleOpened() {
    opened = !opened;
  }
</script>

<AppShell>
  <Navbar slot="navbar" hidden={!opened}>
    <NavContent isDark={isDark} />
  </Navbar>
  <Header slot="header">
    <HeadContent isDark={isDark} toggleTheme={toggleTheme} />
  </Header>

  <slot>This is the main content</slot>
</AppShell>
