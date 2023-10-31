# 前端学习

# Vue 3 + TypeScript + Vite

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support For `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
   1. Run `Extensions: Show Built-in Extensions` from VSCode's command palette
   2. Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.


# 开发详细过程：2023年7月15日15:04:06

## 1、创建vite项目

Vite是一种新型前端构建工具，能够显著提升前端开发体验。

vite官网：<https://cn.vitejs.dev/guide/>

脚手架：create-vite

https://github.com/vitejs/vite/tree/main/packages/create-vite

初始化项目

使用pnpm
```js
create vite
选择vue+ts

cd xops-fe
pnpm install
pnpm run dev
```

## 2、初始依赖

### 初始依赖package.json：
```js
      {
      "name": "xops",
      "private": true,
      "version": "0.1.0",
      "type": "module",
      "scripts": {
         "dev": "vite",
         "build": "vue-tsc && vite build",
         "preview": "vite preview"
      },
      "dependencies": {
         "vue": "^3.3.4"
      },
      "devDependencies": {
         "@vitejs/plugin-vue": "^4.2.3",
         "typescript": "^5.0.2",
         "vite": "^4.4.0",
         "vue-tsc": "^1.8.3"
      }
      }
```
- 2023年8月2日13:53:39

```js
{
  "name": "xops-fe",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vue-tsc && vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "vue": "^3.3.4"
  },
  "devDependencies": {
    "@vitejs/plugin-vue": "^4.2.3",
    "typescript": "^5.0.2",
    "vite": "^4.4.5",
    "vue-tsc": "^1.8.5"
  }
}
```

- 2023年7月15日15:09:02最新版本：

```js
vue： 3.3.4 (2023-05-18)

elment-plus： 2.3.8（2023-07-14）

vuerouter：4.2.4 (2023-07-06)

      https://github.com/vuejs/router

vite： 4.4.4 (2023-07-14)

      https://github.com/vitejs/vite
   
typescript: 5.1.6(2023-07-07)

      https://www.typescriptlang.org/

"@element-plus/icons-vue": "^2.1.0",(2023-mar-4)

      https://github.com/element-plus/element-plus-icons/releases

```
- 2023年8月2日13:54:00最新版本：

```js
vue： 3.3.4 (2023-05-18)

elment-plus： 2.3.8（2023-07-14）

vuerouter：4.2.4 (2023-07-06)

      https://github.com/vuejs/router

vite： 4.4.5 (2023-07-14)

      https://github.com/vitejs/vite
   
typescript: 5.1.6(2023-07-07)

      https://www.typescriptlang.org/

"@element-plus/icons-vue": "^2.1.0",(2023-mar-4)

      https://github.com/element-plus/element-plus-icons/releases

```

### 更新依赖

    1. ncu

      Checking E:\Cillian2023\CIllianTech Projects\Coding Project2023\xops\package.json
      [====================] 5/5 100%

      typescript  ^5.0.2  →  ^5.1.6
      vite        ^4.4.0  →  ^4.4.4
      vue-tsc     ^1.8.3  →  ^1.8.5

    2. nuc -u
   
```js
Using pnpm
Checking E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe\package.json
[====================] 5/5 100%

 typescript  ^5.0.2  →  ^5.1.6
 vite        ^4.4.5  →  ^4.4.8
 vue-tsc     ^1.8.5  →  ^1.8.8

Run ncu -u to upgrade package.json
```

## 3.安装elmentplus和icon
```js
http://element-plus.org/zh-CN/guide/installation.html

pnpm install element-plus

pnpm install @element-plus/icons-vue
```
---
```js
<!-- PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe>  pnpm install element-plus
Packages: +22
++++++++++++++++++++++
Downloading registry.npmjs.org/element-plus/2.3.8: 8.26 MB/8.26 MB, done
node_modules/.pnpm/vue-demi@0.14.5_vue@3.3.4/node_modules/vue-demi: Running postinsnode_modules/.pnpm/vue-demi@0.14.5_vue@3.3.4/node_modules/vue-demi: Running postinstall script, done in 207mssed 46, downloaded 22, added 22, done

dependencies:
+ element-plus 2.3.8
---
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> pnpm install @element-plus/icons-vue
Already up to date

dependencies:
+ @element-plus/icons-vue 2.1.0

Progress: resolved 90, reused 68, downloaded 0, added 0, done
Done in 4.3s -->
```
---


## 4.安装vuerouter

      pnpm install vue-router@latest

      版本：4.2.4

      PS E:\Cillian2023\CIllianTech Projects\Coding Project2023\xops> ncu 
      Using pnpm
      Checking E:\Cillian2023\CIllianTech Projects\Coding    Project2023\xops\package.json
      [====================] 8/8 100%

      All dependencies match the latest package versions :)


## 5.引入配置

#### 全局注册组件

- 引入elment-plus和icon
```js
      // main.ts
      import { createApp } from 'vue'
      import ElementPlus from 'element-plus'
      import 'element-plus/dist/index.css'
      import App from './App.vue'

      const app = createApp(App)

      app.use(ElementPlus)
      app.mount('#app')
```
- Element Plus全局组件类型声明(这个不用了2023年8月2日15:13:19)
```js
// tsconfig.json
{
  "compilerOptions": {
    // ...
    "types": ["element-plus/global"]
  }
}
```


- 引入icon
```js      
      import * as ElementPlusIconsVue from '@element-plus/icons-vue'
      const app = createApp(App)
      for (const [key, component] of Object.entries(ElementPlusIconsVue)) {
      app.component(key, component)
      }
```
页面使用 Element Plus 组件和图标
```js
<!-- src/App.vue -->
<template>
  <img alt="Vue logo" src="./assets/logo.png"/>
  <HelloWorld msg="Hello Vue 3 + TypeScript + Vite"/>
  <div style="text-align: center;margin-top: 10px">
    <el-button :icon="Search" circle></el-button>
    <el-button type="primary" :icon="Edit" circle></el-button>
    <el-button type="success" :icon="Check" circle></el-button>
    <el-button type="info" :icon="Message" circle></el-button>
    <el-button type="warning" :icon="Star" circle></el-button>
    <el-button type="danger" :icon="Delete" circle></el-button>
  </div>
</template>

<script lang="ts" setup>
     import HelloWorld from '/src/components/HelloWorld.vue'
     import {Search, Edit,Check,Message,Star, Delete} from '@element-plus/icons-vue'
</script>

```


- 引入vuerouter

创建文件夹/src/router以及文件index.ts
```js
         const routes = [
      { path: '/', component: Home },
      { path: '/about', component: About },
      ]

      // 3. 创建路由实例并传递 `routes` 配置
      // 你可以在这里输入更多的配置，但我们在这里
      // 暂时保持简单
      const router = VueRouter.createRouter({
      // 4. 内部提供了 history 模式的实现。为了简单起见，我们在这里使用 hash 模式。
      history: VueRouter.createWebHashHistory(),
      routes, // `routes: routes` 的缩写
      })

      // 5. 创建并挂载根实例
      const app = Vue.createApp({})
      //确保 _use_ 路由实例使
      //整个应用支持路由。
      app.use(router)

      app.mount('#app')

      // 现在，应用已经启动了！

```
- main.ts挂载
  
  ```js
  import { createApp } from 'vue'
  import './style.css'
  import App from './App.vue'
  import { router } from './router'


  const app = createApp(App)

  app.use(router)


  app.mount('#app')

#### 路径别名配置

- vite.config.ts配置
- 
      https://cn.vitejs.dev/config/

```js
   import path from 'path'
      resolve:{
            alias:{
               '@':resolve('src'),
               '*':resolve(''),
               'Assets':resolve('src/assets')
            }


2023年8月2日14:59:20
import path from 'path'

export default defineConfig({
    plugins: [vue()],
    resolve: {
        alias: {
            "@": path.resolve("./src") // 相对路径别名配置，使用 @ 代替 src
        }
    }
})
```
### 安装@types/node

```js
这里设置别名有点问题，关于ts的path模块，需要安装ts和@type/node，编译器报错：TS2307: Cannot find module 'path' or its corresponding type declarations.

pnpm install @types/node --save-dev

"@types/node": "^20.4.2",

2023年8月2日14:58:08
 "@types/node": "^20.4.5",

npm会报错，所以全程使用pnpm包管理器
 E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> npm install @types/node --save-dev
npm ERR! code EUNSUPPORTEDPROTOCOL
npm ERR! Unsupported URL Type "link:": link:./src/types

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\cillian\AppData\Local\npm-cache\_logs\2023-08-02T06_45_13_393Z-debug-0.log
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe>  npm install -g npm

下载慢，设置淘宝源
---
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> npm config get registry
https://registry.npmjs.org/
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> 
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> npm config set registry https://registry.npm.taobao.org/       
PS E:\Cillian2023\CillianDevOps\Projects\xops\xops-fe> npm config get registry                                        
https://registry.npm.taobao.org/

```


----
### TypeScript 编译配置

同样还是import path from 'path' 编译报错: TS1259: Module '"path"' can only be default-imported using the 'allowSyntheticDefaultImports' flag

因为 typescript 特殊的 import 方式 , 需要配置允许默认导入的方式，还有路径别名的配置
```js
// tsconfig.json
{
  "compilerOptions": {
    "baseUrl": "./", // 解析非相对模块的基地址，默认是当前目录
    "paths": { //路径映射，相对于baseUrl
      "@/*": ["src/*"] 
    },
    "allowSyntheticDefaultImports": true // 允许默认导入
  }
}
```

## 6.自动导入
Element Plus 官方文档中推荐 按需自动导入 的方式，而此需要使用额外的插件 unplugin-auto-import 和 unplugin-vue-components 来导入要使用的组件。所以在整合 Element Plus 之前先了解下自动导入的概念和作用
为了避免在多个页面重复引入 API 或 组件，由此而产生的自动导入插件来节省重复代码和提高开发效率。
插件	概念	自动导入对象
unplugin-auto-import	按需自动导入API	ref，reactive,watch,computed 等API
unplugin-vue-components	按需自动导入组件	Element Plus 等三方库和指定目录下的自定义组件


https://www.cnblogs.com/haoxianrui/p/17331952.html

## 步骤
```js
pnpm install -D unplugin-vue-components unplugin-auto-import

新建 /src/types 目录用于存放自动导入函数和组件的TS类型声明文件


// vite.config.ts
import { defineConfig } from 'vite'
import AutoImport from 'unplugin-auto-import/vite'
import Components from 'unplugin-vue-components/vite'
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers'

export default defineConfig({
  // ...
  plugins: [
    // ...
    AutoImport({
      resolvers: [ElementPlusResolver()],
    }),
    Components({
      resolvers: [ElementPlusResolver()],
    }),
  ],
})

```
```js
import path from 'path'
import { defineConfig } from 'vite'
import Vue from '@vitejs/plugin-vue'
import Icons from 'unplugin-icons/vite'
import IconsResolver from 'unplugin-icons/resolver'
import AutoImport from 'unplugin-auto-import/vite'
import Components from 'unplugin-vue-components/vite'
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers'
import Inspect from 'vite-plugin-inspect'

const pathSrc = path.resolve(__dirname, 'src')

export default defineConfig({
  resolve: {
    alias: {
      '@': pathSrc,
    },
  },
  plugins: [
    Vue(),
    AutoImport({
      // Auto import functions from Vue, e.g. ref, reactive, toRef...
      // 自动导入 Vue 相关函数，如：ref, reactive, toRef 等
      imports: ['vue'],

      // Auto import functions from Element Plus, e.g. ElMessage, ElMessageBox... (with style)
      // 自动导入 Element Plus 相关函数，如：ElMessage, ElMessageBox... (带样式)
      resolvers: [
        ElementPlusResolver(),

        // Auto import icon components
        // 自动导入图标组件
        IconsResolver({
          prefix: 'Icon',
        }),
      ],

      dts: path.resolve(pathSrc, 'auto-imports.d.ts'),
    }),

    Components({
      resolvers: [
        // Auto register icon components
        // 自动注册图标组件
        IconsResolver({
          enabledCollections: ['ep'],
        }),
        // Auto register Element Plus components
        // 自动导入 Element Plus 组件
        ElementPlusResolver(),
      ],

      dts: path.resolve(pathSrc, 'components.d.ts'),
    }),

    Icons({
      autoInstall: true,
    }),

    Inspect(),
  ],
})
```


### 自动导入图标：

https://github.com/sxzz/element-plus-best-practices/blob/db2dfc983ccda5570033a0ac608a1bd9d9a7f658/vite.config.ts#L21-L58

安装 Element Plus

pnpm install element-plus
安装自动导入 Icon 依赖

pnpm i -D unplugin-icons







### 注意

npm install --save @types/node 和 npm install @types/node 之间的区别在于是否使用了 --save 选项。

npm install --save @types/node 会将 @types/node 包添加到 dependencies 中，并将其保存到 package.json 文件的 "dependencies" 部分。这意味着 @types/node 是项目在生产环境中所需的类型声明依赖。

npm install @types/node 会将 @types/node 包添加到 devDependencies 中，并将其保存到 package.json 文件的 "devDependencies" 部分。这表示 @types/node 是开发过程中所需的类型声明依赖。

@types/node 是一个用于提供 Node.js 的类型声明的包。它提供了 TypeScript 编译器在处理 Node.js 相关代码时所需的类型信息，以提供类型检查和智能提示等功能。在使用 TypeScript 编写 Node.js 项目时，使用 @types/node 是非常常见的做法，以便获得完整的类型支持。

根据你的项目需求，你可以根据需要将 @types/node 添加到相应的依赖部分中。如果你的代码只在开发过程中使用 @types/node，那么将其添加到 devDependencies 中更为合适。如果你的代码在生产环境中也需要使用 @types/node，那么将其添加到 dependencies 中。



#### 这里设置别名有两种
在 Vite 2.x 中设置 src 目录的别名的示例：
      import { defineConfig } from 'vite';
      import path from 'path';

      export default defineConfig({
      resolve: {
         alias: {
            '@': path.resolve(__dirname, 'src'),
         },
      },
      });



import MyComponent from '@/components/MyComponent.vue';

上面配置是基于 ES 模块的语法。如果你的项目使用的是 CommonJS 的模块化规范，可以使用以下代码来进行配置：
```js
// vite.config.js
const { defineConfig } = require('vite');
const path = require('path');

module.exports = defineConfig({
  resolve: {
    alias: {
      '@': path.resolve(__dirname, 'src'),
    },
  },
});
```

ES 模块使用 import 和 export 关键字进行模块的导入和导出，例如：import { foo } from './module';、export default myModule;。

CommonJS 使用 require() 方法进行模块的导入，例如：const foo = require('./module');，并使用 module.exports 或 exports 导出模块。

对于 Vite 和许多现代前端工具而言，它们通常使用 ES 模块化规范，因为 ES 模块有更好的静态分析和构建优化能力，并且可以充分利用浏览器原生的模块加载机制。但是，如果你的项目使用的是 CommonJS 模块化规范，你需要相应地调整配置和代码，例如使用 require() 来导入模块。

到这初步完成配置，可以开始开发了。







- 配置tsconfig.json
```js
   {
   "files": [],
   "references": [
      {
         "path": "./tsconfig.node.json"
      },
      {
         "path": "./tsconfig.app.json"
      }
   ]
   }
```
#### node.json
```js
   {
   "extends": "@tsconfig/node18/tsconfig.json",
   "include": [
      "vite.config.*",
      "vitest.config.*",
      "cypress.config.*",
      "nightwatch.conf.*",
      "playwright.config.*"
   ],
   "compilerOptions": {
      "composite": true,
      "module": "ESNext",
      "types": ["node"]
   }
   }
   ```
#### app.json
```js
      {
      "extends": "@vue/tsconfig/tsconfig.dom.json",
      "include": ["env.d.ts", "src/**/*", "src/**/*.vue"],
      "exclude": ["src/**/__tests__/*"],
      "compilerOptions": {
         "composite": true,
         "baseUrl": ".",
         "paths": {
            "@/*": ["./src/*"]
         }
      }
      }
```
## 7.安装windicss

https://cn.windicss.org/

点击vite

npm i -D vite-plugin-windicss windicss

引入vite.config.js
import WindiCSS from 'vite-plugin-windicss'
plugins: [vue(),WindiCSS()],

引入main.ts
import 'virtual:windi.css'


### Unknown at rule @applycss(unknownAtRules)问题解决

猜想：大致应该是内置的css检查，不识别外置的css规则

https://zhuanlan.zhihu.com/p/624435959
https://github.com/tailwindlabs/tailwindcss/discussions/5258

这个先不着急解决吧

2023年7月16日11:11:00
安装在开发环境依赖
npm install --save-dev stylelint stylelint-config-standard

添加Stylelint配置

创建一个stylelint.config.js文件

module.exports = {
  extends: ["stylelint-config-standard"],
  rules: {
    "at-rule-no-unknown": [
      true,
      {
        ignoreAtRules: [
          "tailwind",
          "apply",
          "variants",
          "responsive",
          "screen",
        ],
      },
    ],
    "declaration-block-trailing-semicolon": null,
    "no-descending-specificity": null,
  },
};

安装Stylelint、Tailwind CSS IntelliSense扩展

在settings中搜索code
编辑settings.json

禁用CSS内置验证

"css.validate": false,
"less.validate": false,
"scss.validate": false,


重启vs警告消失

### windi设置别名

export default {
  alias: {
    'hstack': 'flex items-center',
    'vstack': 'flex flex-col',
    'icon': 'w-6 h-6 fill-current',
    'app': 'text-red',
    'app-border': 'border-gray-200 dark:border-dark-300',
  },
}
https://juejin.cn/post/7025573702855032840

import { defineConfig } from 'windicss/helpers'
import formsPlugin from 'windicss/plugin/forms'

export default defineConfig({
  darkMode: 'class',
  safelist: 'p-3 p-4 p-5',
  theme: {
    extend: {
      colors: {
        teal: {
          100: '#096',
        },
      },
    },
  },
  plugins: [formsPlugin],
})

extract: {
    // A common use case is scanning files from the root directory
    include: ['**/*.{vue,html,jsx,tsx}'],
    // if you are excluding files, make sure you always include node_modules and .git
    exclude: ['node_modules', '.git', 'dist'],
  },


### 注意

1. 一个项目尽量用一种包管理器，比如只使用npm或者pnpm

尽量用npm可以更新package.json
可以使用ncu
2. vue-cli构建转向vite构建，代码需要改动
   比如静态资源的引入

   Uncaught (in promise) ReferenceError: require is not defined 一模一样的代码在vuecli构建正常，使用vite报这个错
```js
   这个错误表明在使用 Vite 构建时，出现了 "ReferenceError: require is not defined" 错误。这是因为 Vite 使用了 ES 模块的导入方式，而不支持使用 CommonJS 的 require 导入语法。

在 Vue CLI 中，可以使用 require 导入静态资源文件（如图片、样式表等），因为 Vue CLI 使用了 Webpack 这样的构建工具，它支持 CommonJS 模块语法。

但是，在 Vite 中，它采用了现代的 ES 模块系统和原生的浏览器导入机制。因此，当你在 Vite 项目中使用 require 时，会导致 "ReferenceError: require is not defined" 错误。

要在 Vite 中正确导入静态资源文件，你可以使用 ES 模块导入语法，如下所示：

javascript
Copy code
import avator from '@/assets/avator/avator.jpg';
import logo from '@/assets/k8s/icon.png';

// 使用导入的静态资源文件
或者，如果你只是想简单地将静态资源文件作为 URL 字符串引入，可以直接在模板中使用相对路径：

html
Copy code
<template>
  <div>
    <img :src="require('@/assets/avator/avator.jpg')" alt="Avator">
    <img :src="require('@/assets/k8s/icon.png')" alt="Logo">
  </div>
</template>
请注意，以上代码示例适用于 Vue 3 和 Vite。在迁移代码时，你需要将 require 语法替换为适用于 Vite 的 ES 模块导入方式。

```

## 8.vue cli转移vite构建

```js

如果你想将一个使用 Vue CLI 创建的项目转换为使用 Vite 构建，以下是一些需要注意的事项：

项目结构： Vue CLI 和 Vite 的项目结构有所不同。在迁移之前，你需要了解 Vite 的项目结构并相应地调整你的文件和目录。

配置文件： Vue CLI 使用 vue.config.js 文件进行项目配置，而 Vite 使用 vite.config.js 文件。你需要将现有的配置从 vue.config.js 移动到 vite.config.js 中，并相应地调整配置选项。

依赖项： Vite 使用不同的依赖项来支持其构建过程。你需要将 Vue CLI 的依赖项转换为 Vite 的对应依赖项。确保查阅 Vite 的文档，了解它所需的依赖项和版本要求。

插件和扩展： 如果你在 Vue CLI 项目中使用了一些特定的插件或扩展，你需要查看是否有对应的 Vite 版本或替代方案。有些插件可能不直接兼容 Vite，需要你寻找相应的 Vite 插件或重新实现所需功能。

构建命令和开发服务器： Vue CLI 使用 npm run serve 命令启动开发服务器，而 Vite 使用 npm run dev。确保将现有的命令更新为适用于 Vite 的命令。

CSS 预处理器： 如果你在 Vue CLI 项目中使用了 CSS 预处理器（如 Sass 或 Less），你需要确保 Vite 的配置中包含相应的插件和配置，以便在 Vite 中继续使用它们。

自定义配置和功能： 如果你在 Vue CLI 项目中有自定义配置或功能，例如自定义 webpack 配置或自定义构建脚本，你需要将其转换为适用于 Vite 的对应方式。Vite 提供了一些扩展配置选项和插件系统，可以帮助你实现自定义需求。
```



## 9.开发开始

### 后台管理系统
涉及技术栈：
      vue3 setup语法糖
      vite构建工具
      vuex状态管理
      vue-router路由管理
      windicss、tailwindcss框架
      elmentplus组件库
      vueuse工具库
      axios
功能：

图表： echarts
用户管理
权限管理
菜单管理


