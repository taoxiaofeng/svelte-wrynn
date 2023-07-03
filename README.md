# 项目配置

```js
node 16.20.0
vite@4.3.9
svelte@4.0.1
```

## 创建项目

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app

# Choose your packages
yarn add dayjs @svelteuidev/prism @svelteuidev/preprocessors @svelteuidev/motion @svelteuidev/dates @svelteuidev/core @svelteuidev/composables

# or
npm i dayjs @svelteuidev/prism @svelteuidev/preprocessors @svelteuidev/motion @svelteuidev/dates @svelteuidev/core @svelteuidev/composables
```

## 安装项目依赖

使用 `npm install` (or `pnpm install` or `yarn`) 安装项目依赖

## 启动项目

```bash
npm run start

# or start the server and open the app in a new browser tab
npm run start -- --open

# yarn
yarn start
```

## 构建

```bash
npm run build

# yarn
yarn build
```

## 项目目录



```
svelte-wrynn
├─ .gitignore   // git 忽略文件
├─ .npmrc       // npm 配置文件
├─ .svelte-kit  // svelte-kit 用于存储与SvelteKit构建过程相关的配置和文件
│  ├─ ambient.d.ts // 用于存储全局类型声明  
│  ├─ generated // 用于存储SvelteKit生成的文件
│  │  ├─ client // 用于存储SvelteKit生成的客户端文件
│  │  │  ├─ app.js // 用于存储SvelteKit生成的客户端应用程序
│  │  │  ├─ matchers.js // 用于存储SvelteKit生成的客户端匹配器
│  │  │  └─ nodes   // 用于存储SvelteKit生成的客户端节点
│  │  │     ├─ 0.js  
│  │  │     ├─ 1.js
│  │  │     ├─ 2.js
│  │  │     ├─ 3.js
│  │  │     ├─ 4.js
│  │  │     └─ 5.js
│  │  ├─ root.svelte // 用于存储SvelteKit生成的根组件
│  │  └─ server   // 用于存储SvelteKit生成的服务器文件
│  │     └─ internal.js   // 用于存储SvelteKit生成的服务器内部文件
│  ├─ tsconfig.json   // 用于存储SvelteKit的TypeScript配置
│  └─ types   //  用于存储SvelteKit的TypeScript类型
│     ├─ route_meta_data.json   // 用于存储SvelteKit生成的路由元数据
│     └─ src
│        └─ routes
│           ├─ $types.d.ts
│           ├─ about
│           │  └─ $types.d.ts  
│           └─ sverdle
│              ├─ $types.d.ts
│              └─ how-to-play
│                 └─ $types.d.ts
├─ README.md  // 项目说明
├─ package.json // 项目依赖
├─ src  // 项目源码
│  ├─ app.d.ts // 用于存储SvelteKit的TypeScript类型
│  ├─ app.html // 用于存储SvelteKit的应用程序HTML模板
│  ├─ lib // 用于存储SvelteKit的应用程序库
│  │  └─ images // 用于存储SvelteKit的应用程序图像
│  │     ├─ github.svg
│  │     ├─ svelte-logo.svg
│  │     ├─ svelte-welcome.png
│  │     └─ svelte-welcome.webp
│  └─ routes // 用于存储SvelteKit的应用程序路由
│     ├─ +layout.svelte // 用于存储SvelteKit的应用程序布局
│     ├─ +page.svelte // 用于存储SvelteKit的应用程序页面
│     ├─ +page.ts
│     ├─ Counter.svelte
│     ├─ Header.svelte
│     ├─ about
│     │  ├─ +page.svelte
│     │  └─ +page.ts
│     ├─ styles.css
│     └─ sverdle
│        ├─ +page.server.ts
│        ├─ +page.svelte
│        ├─ game.ts
│        ├─ how-to-play
│        │  ├─ +page.svelte
│        │  └─ +page.ts
│        ├─ reduced-motion.ts // 用于存储SvelteKit的应用程序减少动作
│        └─ words.server.ts   // 用于存储SvelteKit的应用程序服务器端路由
├─ static // 用于存储SvelteKit的静态文件
│  ├─ favicon.png
│  └─ robots.txt
├─ svelte.config.js // 用于存储SvelteKit的配置
├─ tsconfig.json    // 用于存储SvelteKit的TypeScript配置
├─ vite.config.ts   // 用于存储SvelteKit的Vite配置
└─ yarn.lock        // 用于存储SvelteKit的Yarn依赖

```