# eslint-config-fh

## 手动接入

```bash
npm install --save-dev eslint eslint-config-fh
```

## 项目配置

### 基础 JavaScript 项目

针对未使用 React 或 Vue 的原生 JavaScript 项目，使用 ESLint 原生规则和 [eslint-plugin-import](https://www.npmjs.com/package/eslint-plugin-import) 规则，使用 [@babel/eslint-parser](https://www.npmjs.com/package/@babel/eslint-parser) 作为 parser，是本包的默认配置。

ESLint 配置：

```json
{
  "extends": ["eslint-config-fh"]
}
```

### 基础 TypeScript 项目

针对未使用 React 或 Vue 的 TypeScript 项目，继承了默认配置，并启用了 [@typescript-eslint/eslint-plugin](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/eslint-plugin) 插件的规则，使用 [@typescript-eslint/parser](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/parser) 作为 parser。

ESLint 配置：

```json
{
  "extends": ["eslint-config-fh/typescript"]
}
```

### Vue JavaScript 项目

针对 JS Vue 的项目，继承了默认配置，并启用了 [eslint-plugin-vue](https://www.npmjs.com/package/eslint-plugin-vue) 插件的规则，使用 [vue-eslint-parser](https://www.npmjs.com/package/vue-eslint-parser) 作为 parser。

ESLint 配置：

```json
{
  "extends": ["eslint-config-fh/vue"]
}
```

### Vue TypeScript

针对 TS Vue 项目，继承了 JS Vue 的配置，并启用了 [@typescript-eslint/eslint-plugin](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/eslint-plugin) 插件的规则，使用 [@typescript-eslint/parser](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/parser) 作为 parser。

ESLint 配置：

```json
{
  "extends": ["eslint-config-fh/typescript/vue"]
}
```

注意：需要保证项目安装了 `typescript@5` 依赖，同时根目录下有 `tsconfig.json` 文件。
