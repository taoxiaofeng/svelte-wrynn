# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## 项目目录

```bash
.
│-- .svelte-kit             // .svelte-kit 是由 Kit 在每次编译过程中生成，构建的结果会暂存在这个目录下
│-- src                     // 源码目录
│   │-- app.d.ts
│   │-- app.html
│   │-- routes // 路由页面文件目录
│       │-- +layout.svelte
│       │-- +page.svelte
│       │-- about
│       │   │-- +page.svelte
│       │-- albums
│       │   │-- +page.svelte
│       │-- article
│           │-- +page.svelte
│           │-- bulletin.svelte
│           │-- error.svelte
│           │-- post-list.svelte
│           │-- tags.svelte
│-- static                // 静态文件存放目录
    │-- favicon.png
│-- .gitignore
│-- .npmrc
│-- README.md
│-- list.txt
│-- package.json
│-- svelte.config.js    // kit 配置项
│-- tree.text
│-- tsconfig.json
│-- vite.config.ts   // vite 编译打包配置文件
│-- yarn.lock
```
