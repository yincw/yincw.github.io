---
order: 2
---

# 代码

## 语法高亮

- `javascript`/`typescript`/`js`/`ts`/`vue` 
- `html`/`jsx`/`tsx`
- `css`/`less`/`scss`
- `json`/`yaml`/`yml`
- `markdown`/`md`/`mdx`
- `graphql`/`gql`
- `text`/`txt`/`plain`
- `dart`
- `ansi`
- `sh`

::: code-group

```javascript [js]
export default {
  name: 'MyComponent'
  // ...
}
```

```typescript [ts]
export default {
  name: 'MyComponent'
  // ...
}
```

```html [html]
<ul>
  <li v-for="todo in todos" :key="todo.id">
    {{ todo.text }}
  </li>
</ul>
```

```jsx [jsx]
export default function () {
  return (
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
      </li>
    </ul>
  );
}
```

```css [css]
.text-center {
  text-align: center;
}
```

```less [less]
.text {
  &-center {
    text-align: center;
  }
}
```

```vue [vue]
<template>
<ul>
  <li v-for="todo in todos" :key="todo.id">
    {{ todo.text }}
  </li>
</ul>
</template>
<script>
export default {
  name: 'MyComponent'
  // ...
}
</script>
<style>
.text-center {
  text-align: center;
}
</style>
```


```json [json]
{
  "scripts": {
    "docs:dev": "vitepress dev docs",
    "docs:build": "vitepress build docs",
    "docs:preview": "vitepress preview docs"
  },
}
```

:::


## 代码行高亮及编号

- 编号
  - `:line-numbers` 行号
  - `:line-numbers=2` 设置行号起始值，从2开始编号
- 高亮
  - `{4}` 单行
  - `{6-8}` 多行
  - `// [!code highlight]` 单行
- 聚焦
  - `// [!code focus]` 单行聚焦它并模糊代码的其他部分
  - `// [!code focus:<lines>]` 指定多行聚焦它并模糊代码的其他部分
- diff
  - `// [!code --]` 为该行创建 diff，同时保留代码块的颜色
  - `// [!code ++]` 为该行创建 diff，同时保留代码块的颜色
- 背景色
  - `// [!code warning]` 添加“警告”背景色
  - `// [!code error]` 添加“错误”背景色

```js{4,6-8} :line-numbers
export default { // [!code highlight]
  data () {
    return {
      msg: `Highlighted!
      This line isn't highlighted,  
      but this and the next 2 are.`, // [!code warning]
      motd: 'VitePress is awesome', // [!code error]
      lorem: 'ipsum' // [!code focus]
    }
  }
}
```

## 导入代码片段

- `<<< @/filepath{highlightLines}` 导入代码片段，同时支持行高亮

```
<<< ../demos/demo.vue{3}
```

<<< ../demos/demo.vue{3}

## 组件预览

不支持实时编辑。

- title
- description

```
:::preview  [title] || [description]
```

:::preview demo.vue || Vue SFC 组件预览

demo-preview=../demos/demo.vue

:::

- https://www.npmjs.com/package/@vitepress-demo-preview/plugin

## 组件即时编辑预览

仅支持选项式 API（setup() 写法），不支持 setup 语法糖写法。

- column
- height:400

```
:::demo column height:400
```

:::demo height:300

```vue
<template>
    <div>当前计数为：{{ count }}</div>
    <br />
    <button @click="count++">点我！</button>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const count = ref(0);
    // 其他逻辑...
 
    return { count };
  }
}
</script>
```

:::

- https://www.npmjs.com/package/vitepress-demo-editor

## 组件即时编辑预览(iframe)

iframe 模式。支持 选项式 API（Options） 和 响应式 API（Composition）。但只能配置在 vite.config.ts 文件中，否则报错。

```
``` vue preview  ```
```

```vue preview
<template>
    <div>当前计数为：{{ count }}</div>
    <br />
    <button @click="count++">点我！</button>
</template>

<script setup>
  import { ref } from 'vue';
  const count = ref(0);
</script>
```

- https://vite-plugin-vue-preview.netlify.app/zh/