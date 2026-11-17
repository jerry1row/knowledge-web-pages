# 马哥赢创 · 品牌规范（brand-spec）

> 供本项目所有 HTML 交付物引用。来源：E:/0-马哥知识库

## 品牌资产（本地副本，勿外链用户原目录）

| 资产 | 路径 | 说明 |
|---|---|---|
| Logo（含人设+slogan） | `assets/mage-logo.png` | 1024×1024，奶油底 #F5EFE6，卡通人设（黑框眼镜/黑polo/握拳）+ 橙色上扬箭头 + 黑橙斜体字标「马哥赢创」+ slogan「想法落地 · 价值倍增」 |
| 九宫格表情贴纸 | `assets/mage-stickers.png` | 3×3 表情：微笑/思考/记录/写代码/指点/金币/点赞/惊讶/庆祝。**用 CSS background-position 裁切单格使用**（background-size:300% 300%），位置映射见 mage-manual.css 的 .stk-* 类 |

原文件：`E:/0-马哥知识库/马哥赢创logo.png`、`E:/0-马哥知识库/马哥卡通形象.png`

## 色彩

| Token | 值 | 用途 |
|---|---|---|
| 品牌橙 | `#F5821F` | 主强调、按钮、进度、章节号 |
| 品牌深橙 | `#D96A08` | 链接、强调文字 |
| 品牌浅橙 | `#FFE8D2` / wash `#FFF4E8` | 标签底、hover 底 |
| 纸底 | `#FBF7F0` / 卡 `#FFFDF9` | 页面与卡片背景（小清新奶油纸感） |
| 墨色 | `#1C1B1A` / 次 `#54493D` / 弱 `#94897B` | 文字三级 |
| 描边 | `#EBDFCE` | 卡片/表格边框 |
| 分类色（马卡龙） | 薄荷 `#2F9E6E` / 天蓝 `#2E7EB8` / 黄油 `#B98A00` / 玫红 `#D25454` / 藤紫 `#7C5CF0` | 标签、引用块角标、清单分组点 |

## 字体

- 展示体（标题/章节号/大字）：`ZCOOL QingKe HuangYou`（站酷庆科黄油体，与 logo 黑粗斜气质呼应）
- 正文：`Noto Sans SC`
- 代码/数字：`Space Grotesk` + mono 栈

## 人设信息（用于"马哥说"气泡与页脚）

- 一句话：从普通工薪家庭靠自学和实战成长起来的电商、内容和知识付费操盘者；帮助有经验但不会变现的普通人把能力变成产品
- 主线产品：398 元/年知识星球「马哥AI独立主理人」
- Slogan：想法落地 · 价值倍增

## 表达边界（硬约束，源自个人说明书）

- 不说"保证赚钱/肯定赚钱/买完就有效果/7 天变现/月入过万"
- 结果表达必须带条件（执行时间、内容质量、产品选择、复盘优化）
- 收入/案例/转化率无资料支撑不能写成事实
- 不借具体前公司/品牌做夸张背书

## 交互组件约定（两册共用，见 assets/mage-manual.css / .js）

- 左侧 sticky 目录 + scrollspy + 阅读进度环（.ring）
- 顶部 4px 阅读进度条（#pbar）
- 60 秒速览地图（.mapgrid，点击直达章节）
- 翻转自测卡（.flip，点击翻面看答案）
- 可勾选执行清单（.ckgroup li，localStorage 记忆，key=`mage-manual-ck-<data-book>`）
- 提示词一键复制（.cp 按钮，读同 .fbox 内 pre 文本）
- "马哥说"贴纸气泡（.say，Tweaks 可整体关闭，key=`mage-manual-say`）
- Tweaks 面板：字号 小/中/大（key=`mage-manual-fs`）、马哥说开关、清单重置
- 入场动画 .rv（IntersectionObserver），尊重 prefers-reduced-motion
