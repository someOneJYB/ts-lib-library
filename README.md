# Turborepo starter

This is an official Yarn v1 starter turborepo.

## What's inside?

This turborepo uses [Yarn](https://classic.yarnpkg.com/lang/en/) as a package manager. It includes the following packages/apps:

### Apps and Packages

- `docs`: a [Next.js](https://nextjs.org) app
- `web`: another [Next.js](https://nextjs.org) app
- `ui`: a stub React component library shared by both `web` and `docs` applications
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

## Setup

This repository is used in the `npx create-turbo` command, and selected when choosing which package manager you wish to use with your monorepo (Yarn).

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
yarn run build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
yarn run dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Pipelines](https://turborepo.org/docs/core-concepts/pipelines)
- [Caching](https://turborepo.org/docs/core-concepts/caching)
- [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching)
- [Scoped Tasks](https://turborepo.org/docs/core-concepts/scopes)
- [Configuration Options](https://turborepo.org/docs/reference/configuration)
- [CLI Usage](https://turborepo.org/docs/reference/command-line-reference)

### 好处在于包之间的调试方式更便捷

### packages 专注于 ui 和 utils

### apps 中将补充 react + vite ｜ webpack 项目， react 使用 18 版本

### h5 和 系统，系统采用 tailwind 进行构建，增加 react ssr 项目

### app 目录如下：

### 工程辅助

- [ESLint](https://eslint.org/)
- [stylelint](https://stylelint.io/)
- [Prettier](https://prettier.io/)
- [commitlint](https://commitlint.js.org/)

### 目录结构

```
├── config 配置
├── global.d.ts 全局声明文件
├── mock 文件夹
├── public 文件夹存放 html 文件
├── src
│   ├── assets 公共资源目录
│   │   ├── constants 公共常量目录
│   │   ├── images 公共图片目录
│   │   ├── styles 公共样式目录
│   │   └── utils 公共方法目录
│   ├── components 公共组件目录
│   │   └── component 组件目录
│   │       ├── index.module.less 页面样式文件
│   │       └── index.tsx 页面文件
│   ├── interfaces 公共接口目录
│   ├── pages 页面目录
│   │   └── page1 页面目录
│   │       ├── components页面组件目录
│   │       │   └── component 组件目录
│   │       │       ├── component.module.less 组件样式文件
│   │       │       └── component.tsx 组件文件
│   │       ├── interfaces 页面接口目录
│   │       │   └── index.ts 页面接口文件
│   │       ├── index.module.less 页面样式
│   │       ├── app.tsx 页面结构
│   │       └── index.ts 入口文件
│   └── services 接口目录
└── README.md
```

### css 方案采用 module-css 和 styled-components（运行时的处理使用另一个库）
