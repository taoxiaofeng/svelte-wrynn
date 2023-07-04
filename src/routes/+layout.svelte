<script lang="ts">
  // 为了使 SvelteUI 正常工作，您需要在应用程序的顶层设置 SvelteUIProvider
  import {
    SvelteUIProvider,
    colorScheme,
    Stack,
    Switch,
    Text,
  } from "@svelteuidev/core";
  import Header from "./Header.svelte";
  import "./styles.css";
  import Animation from "../components/Animation.svelte";

  function toggleTheme() {
    colorScheme.update((v) => (v === "dark" ? "light" : "dark"));
  }
</script>

<!-- SvelteUIProvider 包括一个 NormalizeCSS 样式表和一些添加到 body 元素的额外全局样式：

background-color为theme.colors["dark700"].value深色配色方案，浅色为白色
color深色配色方案为theme.colors["dark50"].value，浅色方案为黑色
font-family并font-size根据主题
要启用这些全局样式，请设置withNormalizeCSS和withGlobalStyles道具： -->

<SvelteUIProvider
  withNormalizeCSS
  withGlobalStyles
  themeObserver={$colorScheme}
>
  <div class="app">
    <Header />
    <main>
      <slot />
      <Stack align="center">
        <Text>Press to change the theme</Text>
        <Switch on:change={toggleTheme} />
      </Stack>
      <Animation />
    </main>

    <footer>
      <p>
        visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit
      </p>
    </footer>
  </div>
</SvelteUIProvider>

<style>
  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    width: 100%;
    max-width: 64rem;
    margin: 0 auto;
    box-sizing: border-box;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 12px;
  }

  footer a {
    font-weight: bold;
  }

  @media (min-width: 480px) {
    footer {
      padding: 12px 0;
    }
  }
</style>
