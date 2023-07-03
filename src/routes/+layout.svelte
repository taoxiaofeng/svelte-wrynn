<script lang="ts">
  // 为了使 SvelteUI 正常工作，您需要在应用程序的顶层设置 SvelteUIProvider
  import { pageleave } from "@svelteuidev/composables";
  import { SvelteUIProvider } from "@svelteuidev/core";
  import Header from "./Header.svelte";
  import "./styles.css";
  // import CreateStyles from "../components/CreateStyles.svelte";
  import CreateStyles2 from "../components/CreateStyles2.svelte";
  import CreateStyles3 from "../components/CreateStyles3.svelte";

  let element: any;
  // console.log({ element });
</script>

<!-- SvelteUIProvider 包括一个 NormalizeCSS 样式表和一些添加到 body 元素的额外全局样式：

background-color为theme.colors["dark700"].value深色配色方案，浅色为白色
color深色配色方案为theme.colors["dark50"].value，浅色方案为黑色
font-family并font-size根据主题
要启用这些全局样式，请设置withNormalizeCSS和withGlobalStyles道具： -->

<SvelteUIProvider
  withNormalizeCSS
  withGlobalStyles
  bind:element
  use={[[pageleave, () => console.log("page left")]]}
  class="animate-bounce"
  override={{ mt: "$4" }}
>
  <div class="app">
    <Header />
    <main>
      <slot />
			<CreateStyles3 />
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
