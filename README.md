# Lerna Getting Started Example

This repo is a small example of using Lerna 5+.

Watch this [10-minute walkthrough](https://youtu.be/1oxFYphTS4Y) to see how new versions of Lerna work.

This repo contains three packages or projects:

- `header` (a library of React components)
- `footer` (a library of React components)
- `remixapp` (an app written using the Remix framework which depends on both `header` and `footer`)

```
packages/
    header/
        src/
            ...
        package.json
        rollup.config.json
        jest.config.js

    footer/
        src/
            ...
        package.json
        rollup.config.json
        jest.config.js

    remixapp/
        app/
            ...
        public/
        package.json
        remix.config.js

package.json
```

pnpm recursive run build

### 所有包都安装，可以添加 --filter 过滤

pnpm -r add --save-dev @changesets/cli
pnpm -r remove @changesets/cli

### Root 下安装

pnpm -w add --save-dev @changesets/cli

### changeset 版本管理

pnpm changeset init // 初始化
pnpm changeset add // 添加变更信息
pnpm changeset version // 生成 CHANGELOG.md
pnpm changeset publish // 发布到 npm，自动打 tag
