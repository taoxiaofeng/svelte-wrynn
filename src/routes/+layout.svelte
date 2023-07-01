<!-- <h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
<header>
  <h1>演示</h1>
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/albums">Albums</a></li>
    <li><a href="/about">About</a></li>
  </ul>
</header>

<!-- 内容区 -->
<main>
  <slot />
</main>

<footer>
  CopyRight &copy; 2023
  <a href="www.baidu.com">这是一个演示系统</a>
</footer>
