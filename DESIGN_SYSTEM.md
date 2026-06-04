# Grand Markets Academy 设计系统

## 1. 设计目标

Grand Markets Academy 的设计系统服务于一个中文金融教育与品牌官网。整体视觉应体现：

- 专业金融机构的可信度
- 澳洲持牌教育机构的合规感
- 国际化品牌的克制与秩序
- 课程网站的清晰导航与转化路径

设计关键词：深色、金色、克制、留白、秩序、低噪音、可信、机构级。

## 2. 色彩规范

### 核心色

| 用途 | 色值 | 说明 |
| --- | --- | --- |
| 主背景深蓝 | `#0A1628` | 全站主背景、Footer、Hero 渐变终点 |
| 品牌金色 | `#C9A84C` | 标签、重点数字、图标、按钮、分隔线、当前状态 |
| 白色文字 | `#FFFFFF` | 主标题、重要文字 |
| 次级文字 | `rgba(255,255,255,0.6)` | 段落、说明、Footer 文案 |
| 弱说明文字 | `rgba(255,255,255,0.4)` | 版权、风险提示、二维码说明 |
| 卡片背景 | `rgba(255,255,255,0.06)` | 常规卡片和模块背景 |
| 强卡片背景 | `rgba(255,255,255,0.08)` | hover 或重点模块背景 |
| 细边框 | `rgba(255,255,255,0.1)` | 卡片边框、区块分隔线 |
| 金色弱背景 | `rgba(201,168,76,0.08)` | CTA 区、强调区域底色 |
| 金色弱边框 | `rgba(201,168,76,0.2)` | CTA 或可点击模块边框 |

### 使用原则

- 深蓝是主背景，不再切回大面积白色背景。
- 金色只用于强调，不应大面积铺满。
- 文本不要全部纯白，正文以 `rgba(255,255,255,0.66~0.85)` 更舒适。
- 重要 CTA 可使用金色实心按钮。
- 信息型标签可使用金色文字 + 深色透明底。
- 分隔线使用 `0.5px` 或 `1px` 的低对比度白色透明线。

## 3. 字体规范

### 字体族

```css
font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC",
  "Hiragino Sans GB", "Microsoft YaHei", Arial, sans-serif;
```

### 标题字号

全站标题使用 `clamp()` 自适应，避免中文单字换行不自然。

```css
h1 { font-size: clamp(28px, 4vw, 52px); }
h2 { font-size: clamp(22px, 3vw, 38px); }
h3 { font-size: clamp(16px, 2vw, 24px); }
```

### 页面 Hero 标题

- 首页 Hero：`clamp(32px, 4vw, 52px)`
- 关于我们 Hero：`clamp(24px, 4vw, 42px)`
- 社区页 Hero：`clamp(28px, 4vw, 42px)`
- 其他内页 Hero：建议 `clamp(28px, 4vw, 48px)`

### 正文

- 常规正文：`14px~16px`
- 金融从业与量化页面正文行高：`line-height: 1.8`
- About 品牌叙事段落：`line-height: 1.9`
- Footer 风险声明：`12px`，`line-height: 1.8`
- 小标签：`11px`，大写英文，`letter-spacing: 0.08em~0.12em`

### 换行规则

```css
h1, h2, h3 {
  word-break: keep-all;
  overflow-wrap: break-word;
}

p {
  max-width: 720px;
  line-height: 1.8;
}
```

## 4. 布局规范

### 容器

```css
--max-width: 1160px;
.container {
  width: min(var(--max-width), calc(100% - 32px));
  margin: 0 auto;
}
```

### 区块

- 常规区块：上下 `72px~96px`
- 移动端区块：上下 `42px~58px`
- Hero 区：根据页面性质设置 `60vh~85vh`
- 页面之间通过留白和细分隔线分区，避免使用过多重背景块

### 网格

常用网格：

```css
grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
grid-template-columns: repeat(3, minmax(0, 1fr));
grid-template-columns: repeat(2, minmax(0, 1fr));
```

响应式：

- `1024px` 以下：多列变两列或一列
- `860px` 以下：导航切换为汉堡菜单
- `640px` 以下：大部分内容改为单列

## 5. Header 规范

Header 固定在顶部：

- 背景：`rgba(10, 22, 40, 0.72~0.85)`
- 使用 `backdrop-filter: blur(8px~14px)`
- 高度约 `70px~80px`
- 左侧 Logo 与品牌名
- 右侧导航
- 当前页 `.is-active` 使用金色底线或高亮
- `加入社区` 使用金色边框按钮

手机端：

- 显示汉堡按钮
- 菜单下拉为深色面板
- 导航项单行点击区域足够大

## 6. Footer 规范

Footer 采用最终三栏结构：

### Logo 行

- 左侧 36px 金色 Logo 方块
- 右侧品牌名与副标题
- 底部分隔线

### 三栏

顺序固定为：

1. 快捷导航
2. 监管资质
3. 联系我们

### 风险声明

风险声明必须保留，字号 `12px`，颜色 `rgba(255,255,255,0.4)`，`AFSL #554475` 使用金色高亮。

### 版权栏

- 左侧版权
- 右侧社交图标
- 图标默认灰色，hover 金色

## 7. 按钮规范

### 主按钮

用于主要 CTA，例如加入社区、立即报名、立即咨询。

```css
.btn-primary {
  background: #C9A84C;
  color: #0A1628;
  border: 1px solid #C9A84C;
}
```

建议：

- 圆角：`999px`
- 内边距：`12px 22px`
- 字号：`14px`
- 字重：`700`

### 次按钮

用于 Hero 中的辅助行动。

```css
.btn-secondary {
  background: transparent;
  border: 1px solid rgba(255,255,255,0.5);
  color: #ffffff;
}
```

### 小型详情按钮

用于课程卡片底部的 `了解详情 →`。

```css
border: 1px solid rgba(201,168,76,0.4);
color: #C9A84C;
padding: 6px 16px;
border-radius: 20px;
font-size: 12px;
```

Hover：

```css
background: rgba(201,168,76,0.12);
```

## 8. 卡片规范

### 常规卡片

```css
background: rgba(255,255,255,0.06);
border: 1px solid rgba(255,255,255,0.1);
border-radius: 12px;
padding: 24px;
```

### 卡片文字

- 标题：白色，`16px~20px`
- 正文：`rgba(255,255,255,0.66~0.85)`
- 标签：金色，`11px~12px`

### Hover

可点击卡片建议：

```css
transition: border-color 0.2s ease, transform 0.2s ease, background 0.2s ease;
```

Hover 状态：

```css
border-color: rgba(201,168,76,0.4);
cursor: pointer;
```

### 使用原则

- 课程模块、跳转入口、荣誉图片适合使用卡片。
- About 页、品牌故事页不宜大量堆叠卡片，应优先使用叙事布局、时间线、分组标签、数据条。
- 不要卡片套卡片。

## 9. 表格与列表规范

正式页面中尽量少用传统表格。若需要展示结构化信息，优先使用：

- 细线分隔的信息列表
- 金色编号路径
- 时间线
- 分组标签
- 两列图文布局

只有在对比参数、考试科目、课程表等强结构内容中才使用表格。

表格风格建议：

```css
border: 0.5px solid rgba(255,255,255,0.1);
background: rgba(255,255,255,0.04);
font-size: 14px;
```

表头：

```css
color: #C9A84C;
background: rgba(201,168,76,0.08);
```

## 10. 图片规范

### 图片容器

```css
border-radius: 12px;
overflow: hidden;
background: rgba(255,255,255,0.06);
border: 0.5px solid rgba(255,255,255,0.1);
```

### 图片填充

```css
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

### 图片蒙层

在文字叠加图片时使用：

```css
background: linear-gradient(to bottom, rgba(10,22,40,0.2), rgba(10,22,40,0.6));
```

### 占位原则

- 有明确未来图片的位置可以保留占位。
- 没有图片需求的位置应直接删除灰色占位。
- 真实照片优先于占位块。
- 证照图片可以使用 `object-fit: contain` 或根据视觉裁切调整。

## 11. Hero 规范

### 首页 Hero

- 使用背景图
- `background-size: cover`
- 深色蒙层
- 底部渐变自然衔接深蓝背景
- 内容垂直居中

### About Hero

- 使用金色彩带背景图
- 标题叠加在背景图上
- 深色蒙层 + 底部渐变
- 背景高度目前偏短，利于内容上提

### 普通内页 Hero

- 深蓝背景
- 小标签 + 主标题 + 副标题
- 可选图片占位或学习路径组件
- 不要过度装饰

## 12. 标签与徽章

### 小标签 Eyebrow

```css
color: #C9A84C;
font-size: 11px;
font-weight: 700;
letter-spacing: 0.1em;
text-transform: uppercase;
```

### 圆角徽章

```css
border: 0.5px solid rgba(255,255,255,0.1);
border-radius: 20px;
background: rgba(255,255,255,0.06);
font-size: 11px;
```

### 金色标签

```css
background: rgba(201,168,76,0.12);
color: #C9A84C;
```

## 13. 图标规范

优先使用 Tabler Icons：

- 牌照：`ti-shield-check`
- 证书：`ti-certificate`、`ti-file-certificate`
- 用户：`ti-users`
- 全球：`ti-world`
- 地址：`ti-map-pin`
- 邮件：`ti-mail`
- 电话：`ti-phone`
- 客服：`ti-headset`
- 社交：`ti-brand-facebook`、`ti-brand-instagram`、`ti-brand-youtube`

图标颜色：

```css
color: #C9A84C;
```

常规图标大小：

- 小图标：`16px~18px`
- 卡片图标：`20px~24px`
- 徽章图标：`28px~34px`

## 14. 动画与交互

动画应轻量、克制：

```css
transition: color 0.2s ease, border-color 0.2s ease, background 0.2s ease, transform 0.2s ease;
```

建议使用：

- 按钮 hover 颜色变化
- 可点击卡片边框变金色
- 轻微 `translateY(-2px)`

避免使用：

- 大幅缩放
- 复杂滚动动画
- 眩光、粒子、过度渐变
- 长时间循环动画

## 15. 响应式规范

### Breakpoints

```css
@media (max-width: 1024px) { ... }
@media (max-width: 860px) { ... }
@media (max-width: 640px) { ... }
```

### 1024px 以下

- 三列布局改为两列或一列
- About 叙事布局变为单列
- Footer 三栏可变两列
- 图片和文字上下排列

### 860px 以下

- Header 导航切换为汉堡菜单
- 品牌副标题缩短宽度
- 菜单打开为深色浮层

### 640px 以下

- 大部分网格变为单列
- Hero padding 减小
- 卡片 padding 减小
- Footer 单列堆叠
- Timeline 圆点与文字保持左侧对齐

## 16. 可访问性规范

- 图片必须有 `alt`。
- 可点击卡片若不是 `<a>`，必须有 `role="link"`、`tabindex="0"` 并支持键盘。
- 更推荐整张卡片直接用 `<a>` 包裹。
- 按钮文字应清晰描述动作，例如 `立即报名`、`加入社区获取资料`。
- 图标作为装饰时添加 `aria-hidden="true"`。
- 导航按钮需使用 `aria-expanded` 与 `aria-controls`。

## 17. 页面设计建议

### 首页

使用强 Hero、徽章资质、数据卡片、四大入口，强调品牌可信度和转化路径。

### 关于我们

减少卡片，使用叙事排版、时间线、生态分组、真实图片和数据条，保持品牌故事感。

### 金融从业

课程模块与备考路径可以使用卡片，因为用户需要快速扫描和点击。

### 量化策略

课程系列、模块详情、训练营 CTA 是核心。模块卡片需可点击，路径清晰。

### 活动 & 荣誉

图片优先。荣誉墙与图片墙应使用真实照片，避免过多文字表格。

### 加入社区

保持极简。介绍文字 + 二维码 + 免费入群提示即可，避免复杂卡片。

## 18. 后续维护注意事项

- 新增页面时先复制正式页面的 Header/Footer。
- 不要从旧备份页面复制旧样式。
- 修改 Footer 时必须同步所有正式页面。
- 页面 CSS 版本号可用 query string 更新，避免浏览器缓存。
- 避免在正式页面出现“占位内容”“开发备注”等字样。
- 金融风险提示与教育用途声明必须保留。
