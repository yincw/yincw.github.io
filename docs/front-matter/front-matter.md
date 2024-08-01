# Front Matter

参数 | 类型 | 默认值 | 描述
---|---|---|---
 `layout` | `doc / home / page` | `doc` | 页面模板布局，可选值：`doc`、`home`、`page`以及 `false` 自定义组件名
 `title` | `string` | - | 页面的标题
 `titleTemplate` | `string / boolean` | - | 标题的后缀
 `description` | `string` | - | 页面的描述
 `head` | `HeadConfig[]` | - | 指定要为当前页面注入的额外 head 标签
 `navbar` | `string` | `true` | 是否显示导航栏
 `footer` | `boolean` | `true` | 页脚，当侧边栏可见时，不会显示页脚
 `pageClass` | `string` | - | 将额外的类名称添加到特定页面

- https://vitepress.dev/zh/guide/frontmatter
- https://vitepress.dev/zh/reference/frontmatter-config
- https://vitepress.dev/zh/reference/default-theme-layout

## 文档页相关

参数 | 类型 | 默认值 | 描述
---|---|---|---
 `sidebar` | `boolean` | `true` | 是否显示 侧边栏
 `aside` | `boolean / 'left'` | `true` | 大纲的位置，true 渲染到右侧，left 渲染到左侧
 `outline` | `number / [number, number] / 'deep' / false` | `true` | 大纲中显示的标题级别
 `editLink` | `boolean` | `true` | 编辑链接
 `lastUpdated` | `boolean / Date` | `true` | 最后更新于
 `prev` | `string / false / { text?: string; link?: string }` | false | 上一页
 `next` | `string / false / { text?: string; link?: string }` | false | 下一页

- https://vitepress.dev/zh/reference/default-theme-sidebar
- https://vitepress.dev/zh/reference/default-theme-edit-link
- https://vitepress.dev/zh/reference/default-theme-last-updated
- https://vitepress.dev/zh/reference/default-theme-prev-next-links
- https://vitepress.dev/zh/reference/default-theme-carbon-ads

## 主页相关

参数 | 类型 | 默认值 | 描述
---|---|---|---
 `hero` | `string` | - | 用于定义模块的名称、描述、标签、图标等信息
 `features` | `string / boolean` | - | 模块的特色

- https://vitepress.dev/zh/reference/default-theme-home-page
- https://vitepress.dev/zh/reference/default-theme-footer

## 团队页相关

- VPTeamPage 
  - VPTeamPageTitle 
    - #title
    - #lead
  - VPTeamMembers 
    - size  =>  medium、small
    - :members
  - VPTeamPageSection
    - #title
    - #lead
    - #members
      - VPTeamMembers

- https://vitepress.dev/zh/reference/default-theme-team-page

## 站点配置相关

- https://vitepress.dev/zh/reference/site-config
- https://vitepress.dev/zh/reference/default-theme-nav

## 主题配置相关

- 自动生成侧边栏
  - https://vitepress-sidebar.jooy2.com/
- 本地文档搜索
  - https://github.com/emersonbottero/vitepress-plugin-search
  - https://vitepress.dev/zh/reference/default-theme-search
- https://vitepress.dev/zh/reference/default-theme-config
