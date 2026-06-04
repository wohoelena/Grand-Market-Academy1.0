# Grand Markets Academy 项目上下文

## 1. 项目定位

Grand Markets Academy（GMA）是 Grand Markets Group 面向中文用户建立的金融教育与品牌展示网站。网站当前采用纯 HTML、CSS 和少量 JavaScript 构建，定位为一个专业、克制、国际化的金融教育门户，用于承载集团背景、监管资质、RG146 金融从业培训、量化策略课程、活动荣誉与私域社区入口。

项目不是营销型单页，也不是复杂后台系统。它更接近一个“品牌官网 + 课程入口 + 社区转化”的多页面静态网站。页面内容需要保持金融机构应有的可信度、合规感与视觉秩序，避免过度娱乐化或过度装饰。

## 2. 品牌与业务背景

Grand Markets Group 成立于 2020 年，总部位于澳大利亚悉尼，业务覆盖六个国家和地区，团队规模超过 200 人。集团持有澳洲 ASIC 金融服务牌照（AFSL #554475）、毛里求斯 FSC 牌照，以及 Comoros MISA 离岸合规框架。

集团业务和生态包含：

- 100% 控股子公司：Grand Markets Academy、Grand Markets Trading、Grand Markets Australia、Grand Markets Mauritius、Grand Markets HongKong、Grand Markets Capital、Grand Markets Tech。
- 集团持股公司：TraceVaults（链上风控与 AML 监测）、Jade Days Pty Ltd（中国旅游服务）。
- 战略合作伙伴：CICC、中金公司相关大宗商品机构合作、PandaAI、LMAX 等机构与科技生态伙伴。
- 参与组织与协会：United Nations Global Compact、FinTech Australia 等。
- 品牌活动与荣誉：Wiki Finance Expo 获奖、CIIE 参展与感谢信、央视品牌强国企业签约、澳大利亚总理慈善晚宴、广东卫视新春晚会等。

## 3. 目标用户

网站主要服务以下用户群体：

- 在澳留学生：希望毕业后进入金融、理财、交易、合规或金融科技相关行业。
- 新移民与职业转型者：希望了解澳洲金融从业资格与 RG146 备考路径。
- 金融从业者：需要满足 ASIC 合规要求，补考、晋升或进入 AFSL 持牌机构。
- 机构客户与专业交易者：关注 GM 集团背景、监管资质、交易基础设施与全球合作生态。
- 量化学习者与编程兴趣者：希望从零理解量化策略、EA 自动化交易、Python 量化与 AI 量化研究。
- 潜在社区成员：希望加入 GMA 社群，获取课程资讯、活动预告、行业洞察与导师支持。

## 4. 设计风格

当前全站采用深色金融风格：

- 主背景：深蓝 `#0A1628`
- 品牌重点色：金色 `#C9A84C`
- 主文字：白色
- 次要文字：低对比度白色透明色
- 卡片/模块：半透明深色面板，轻边框，弱阴影或无阴影
- 图标：优先使用 Tabler Icons outline 风格
- 图片：真实图片优先，缺图时使用克制的占位块，避免大量灰色占位影响质感

整体视觉目标是“专业金融机构 + 国际品牌 + 教育学院”。设计应保持：

- 克制、清晰、可信
- 少用重卡片和复杂装饰
- 强调内容层级、留白和细分隔线
- 使用金色作为导向、标签、重点数字和图标色
- 避免一屏内出现过多同质卡片
- 避免大面积浅色块破坏深色品牌统一性

## 5. 技术结构

项目使用：

- HTML5
- CSS3
- 少量原生 JavaScript
- Google Fonts 引入 Inter
- Tabler Icons Webfont
- 无前端框架
- 无构建流程

当前主要资源目录：

- `css/style.css`：全站样式与页面专属样式。
- `js/nav.js`：移动端导航与卡片跳转交互。
- `assets/`：Logo、真实图片、活动图片、牌照图片等。
- `images/`：Hero 背景图等站点图片。

## 6. 当前页面结构

### 核心页面

- `index.html`：首页，包含 Hero、资质徽章、核心数据、板块入口。
- `about.html`：关于我们，包含品牌介绍、集团架构、发展历程、牌照合规、合作生态、社会责任、数据栏。
- `rg146.html`：金融从业，包含 RG146 备考中心、人群、三大课程模块、详情区、CTA。
- `quant.html`：量化策略，包含三大课程系列、课程详情、作品集、训练营报名。
- `events.html`：活动 & 荣誉，包含活动荣誉 Hero、数据栏、荣誉墙、图片墙。
- `community.html`：加入社区，包含社区 Hero、介绍文字、二维码区、入群提示。

### RG146 子页面

- `rg146-exam.html`：考试科目与备考路径主页面。
- `rg146-generic.html`：Generic Knowledge 模块。
- `rg146-specialist.html`：Specialist 模块。
- `rg146-schedule.html`：学习周期规划。
- `rg146-mock.html`：模拟测试与题库。

### Quant 子页面

- `quant-auto.html`：自动化策略开发教程主页面。
- `quant-auto-env.html`：编程环境搭建。
- `quant-auto-logic.html`：策略逻辑编写。
- `quant-auto-backtest.html`：回测与优化。
- `quant-auto-deploy.html`：实盘部署。
- `quant-python.html`：Python 量化策略课主页面。
- `quant-python-basics.html`：Python 量化基础。
- `quant-python-signal.html`：策略信号开发。
- `quant-python-backtest.html`：回测框架搭建。
- `quant-python-pandaai.html`：PandaAI 量化实战。

### 旧页面或待整理页面

项目根目录仍存在一些早期页面，如 `courses.html`、`knowledge.html`、`learning-path.html`、`compliance.html`、`topic.html`、`traders.html` 等，以及多个备份目录。后续正式上线前应确认这些页面是否需要保留、重构、重定向或删除，避免用户进入旧版乱码或旧设计页面。

## 7. 全站共用结构

### Header

所有正式页面应复用统一顶部固定导航栏：

- 左侧：GMA Logo + `Grand Markets Academy`
- 副标题：`澳洲持牌金融教育机构 · AFSL 554475`
- 右侧导航：首页 / 金融从业 / 量化策略 / 活动 & 荣誉 / 关于我们 / 加入社区
- 当前页使用 `.is-active`
- 加入社区使用金色边框按钮风格
- 手机端使用汉堡菜单

### Footer

所有正式页面应复用统一 Footer：

- Logo 行独占全宽
- 三栏：快捷导航 / 监管资质 / 联系我们
- 风险声明区
- 版权栏与社交媒体图标

风险声明文案必须保留，并突出 `AFSL #554475`。

## 8. 开发原则

### 内容原则

- 金融相关页面必须保持教育与合规表述，不暗示收益承诺。
- 所有课程内容应表达为教育用途、学习路径或训练营信息。
- 涉及交易、投资、金融产品时，避免使用“保证盈利”“稳定收益”“稳赚”等表达。
- 真实证照、活动、合作、奖项内容应尽量搭配图片或清晰来源说明。

### 结构原则

- 页面优先使用清晰的区块结构：Hero、导语、主体内容、CTA、Footer。
- 大页面应减少重复卡片，优先使用故事线、分组列表、数据条、视觉图文组合。
- 课程页面可以使用卡片，因为课程模块天然适合网格入口。
- 品牌介绍页应更像叙事页面，少用后台表格感。

### 代码原则

- 保持纯 HTML + CSS + 少量 JS，不引入框架。
- 页面跳转全部使用相对路径。
- 新页面必须复用现有 Header、Footer 和 `css/style.css`。
- 图标优先使用 Tabler Icons。
- 新增样式优先复用变量，如 `--navy`、`--gold`、`--muted`、`--line`。
- 页面专属样式可以写入 `style.css`，但 class 命名要清晰，避免影响其他页面。
- 修改 CSS 后建议更新页面中的 CSS query version，避免浏览器缓存。

## 9. 图片与资产原则

当前项目已使用真实图片资源：

- 首页 Hero 背景：`images/hero-bg.jpg`
- 关于我们 Hero 背景：`images/Header_youtube-02.jpg`
- 牌照图片：`assets/photos/mauritius-fsc-license.png`、`assets/photos/comoros-misa-license.png`
- 活动图片：Wiki Expo、CIIE、CCTV 签约、总理晚宴、PandaAI 活动等
- 社会责任图片：`assets/photos/ungc-new-participant.png`

未来添加图片时建议：

- 使用语义化文件名，避免空格和中文文件名。
- 放入 `assets/photos/` 或 `images/`。
- 活动/证照/品牌素材优先使用真实图。
- 缺图位置不一定保留灰色占位，除非该位置未来明确需要图片。
- 图片应设置 `alt` 文案，方便可访问性和后续 SEO。

## 10. 未来规划

### 第一阶段：上线前整理

- 清理旧页面和备份目录，明确正式上线页面集合。
- 检查所有页面 Header/Footer 是否一致。
- 检查所有页面是否引用同一套深色设计系统。
- 检查所有内部链接是否可点击。
- 检查移动端导航、课程卡片、模块卡片跳转。
- 替换所有无意义占位内容。

### 第二阶段：内容完善

- 补充 RG146 课程真实文案、考试信息、FAQ。
- 补充量化策略课程真实模块内容、讲师介绍、课程大纲。
- 补充社区二维码真实图片。
- 完善活动 & 荣誉图片与对应说明。
- 完善关于我们中的办公室、团队、合作素材。

### 第三阶段：品牌与转化增强

- 增加课程报名表单或外部报名入口。
- 增加 FAQ、常见问题、报名流程说明。
- 增加用户案例或学员反馈，但必须避免金融收益承诺。
- 增加 SEO metadata、Open Graph 图片、站点地图整理。
- 若需要多语言，可规划中英双语结构。

### 第四阶段：技术增强

- 可选加入轻量构建工具或静态站点生成器，但不是当前必须。
- 可选将 Header/Footer 抽成模板，减少重复 HTML。
- 可选加入简单表单后端、CRM 表单、邮件通知或二维码统计。
- 可选加入图片压缩与自动缓存版本管理。

## 11. 当前维护重点

当前最重要的维护方向是：

- 保持深色金融风格统一。
- 减少“临时占位”和“开发备注”出现在正式页面。
- 统一 Footer 与风险声明。
- 优化 About、Events 等品牌页面的叙事感。
- 保持 RG146 和 Quant 课程页面的可点击层级清晰。
- 上线前处理旧页面、备份目录和可能的乱码入口。
