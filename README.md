# 金融底层逻辑学习框架

以黄金为锚，把零散的金融知识整理成一条可复用的因果链：

**机会成本（实际利率）→ 美元 → 信用风险与央行购金 → 资产价格**

不是背宏观指标，而是理解每个指标通过哪条链影响预期。配套的交互学习页包含 **6 个模块、18 道自测、相似题重测和判断句生成器**，学习进度自动保存在本地浏览器。

<p>
  <a href="https://zhaangzee.github.io/zhaangzee-215ing/"><img src="https://img.shields.io/badge/开始学习-在线交互版-176b51?style=for-the-badge" alt="开始学习"></a>
  <a href="gold-finance-logic/SKILL.md"><img src="https://img.shields.io/badge/查看内容-Skill%20%E6%96%87%E6%A1%A3-a8730f?style=for-the-badge" alt="查看 Skill 文档"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-17201c?style=for-the-badge" alt="MIT License"></a>
</p>

> 在线版：<https://zhaangzee.github.io/zhaangzee-215ing/>
>
> 如果页面尚未完成首次部署，可在仓库的 **Actions** 页面等待 `Deploy interactive guide` 运行完成。

---

## 学习入口

| 入口 | 适合场景 |
| --- | --- |
| [在线交互学习页](https://zhaangzee.github.io/zhaangzee-215ing/) | 直接开始学习，无需下载 |
| [本地 HTML 页面](gold-finance-logic/assets/finance-logic-framework.html) | 查看或修改网页源码 |
| [Skill 工作流](gold-finance-logic/SKILL.md) | 让 WorkBuddy 用这套框架分析事件、出题带练 |
| [知识底稿](gold-finance-logic/references/finance_logic.md) | 查阅完整理论与案例，作为内容维护的唯一依据 |

> GitHub 文件预览中的 `.html` 会显示源码，而不是网页。要直接打开学习页，请使用上面的在线入口。

## 你会学到什么

- 为什么黄金可以被概括为 **“机会成本 + 保险价值”**。
- CPI、非农、美联储表态、美元和地缘风险分别通过哪条链传导。
- 为什么 CPI 很高时黄金可能下跌，降息时黄金也可能不涨。
- 如何区分需求型通胀、供给型通胀与信用风险。
- 如何用七步法把宏观判断整理成一句可检验的话。
- 如何用自测与相似题发现“看懂了但没真正掌握”的知识缺口。

## 学习路线

| 模块 | 主题 | 关键问题 |
| --- | --- | --- |
| 01 | 黄金是什么 | 黄金凭什么跨文明、跨时代被信任？ |
| 02 | 四层传导 | 宏观数据如何经过政策预期到达金价？ |
| 03 | 三条底层链 | 机会成本、美元、风险信用，哪条链正在主导？ |
| 04 | 五大反转 | 哪些直觉在特定环境下会失效？ |
| 05 | 三个反常案例 | 布雷顿森林、日本通缩、俄罗斯外储说明了什么？ |
| 06 | 实战判断法 | 如何先定环境、再定主链，最后用价格确认？ |

## 核心模型

**黄金价格 = 持有它的机会成本 + 持有它的保险价值**

- **机会成本**：美债实际收益率越高，持有无息黄金的代价越大。
- **保险价值**：美元信用、地缘风险、制裁与央行购金共同抬高长期底部。

一句话记忆：

> 中短期看「实际利率 + 美元」，长周期看「信用 + 央行购金」。

一切宏观指标都只是改变「实际利率 / 美元 / 信用预期」的入口，而不是价格的直接原因。

## 快速开始

### 在线使用

直接打开：

<https://zhaangzee.github.io/zhaangzee-215ing/>

学习记录存放在浏览器 `localStorage`，换浏览器或清理站点数据后会重置。

### 本地打开

```bash
git clone https://github.com/zhaangzee/zhaangzee-215ing.git
cd zhaangzee-215ing
```

双击根目录的 `index.html`，或直接用浏览器打开：

```text
gold-finance-logic/assets/finance-logic-framework.html
```

如需本地服务器预览：

```bash
python -m http.server 8000
```

然后访问 `http://localhost:8000/`。

### 安装为 WorkBuddy Skill

Skill 适合让 WorkBuddy 在后续对话中自动调用这套框架，分析 CPI、美联储、地缘风险或生成练习题。

**macOS / Linux：**

```bash
mkdir -p "$HOME/.workbuddy/skills"
cp -r gold-finance-logic "$HOME/.workbuddy/skills/gold-finance-logic"
```

**Windows PowerShell：**

```powershell
New-Item -ItemType Directory -Force "$HOME\.workbuddy\skills" | Out-Null
Copy-Item -Recurse -Force ".\gold-finance-logic" "$HOME\.workbuddy\skills\gold-finance-logic"
```

安装后可直接提出：

- “用这套框架分析今晚的 CPI。”
- “按每节 3 题带我自测。”
- “我答错了，给一道结构相同但措辞不同的相似题。”

## 项目结构

```text
zhaangzee-215ing/
├── index.html                          # GitHub Pages 入口
├── README.md                           # 项目说明与学习入口
├── LICENSE                             # MIT License
├── .github/
│   └── workflows/
│       └── pages.yml                   # GitHub Pages 自动部署
└── gold-finance-logic/                 # WorkBuddy Skill
    ├── SKILL.md                        # 触发条件、工作流与使用约束
    ├── README.md                       # Skill 目录说明
    ├── references/
    │   └── finance_logic.md            # 完整知识底稿
    └── assets/
        └── finance-logic-framework.html # 交互学习页
```

## 内容维护

- 理论口径以 `gold-finance-logic/references/finance_logic.md` 为准。
- 网页中的课程数据位于 `gold-finance-logic/assets/finance-logic-framework.html` 的 `COURSE` 常量。
- 修改后先在桌面与手机宽度下检查章节展开、答题反馈、相似题重测和判断句生成器。
- 仓库推送到 `main` 分支后，GitHub Actions 会自动更新在线页面。

> 具体行情数字只作为历史案例，不应脱离发生时间和市场背景使用。分析新事件时请使用最新数据。

## 免责声明

本项目所有内容均为金融认知学习材料，用于建立底层思维框架，**不构成任何投资建议**。市场有风险，投资决策需独立判断，并咨询具备相应资质的专业人士。

## License

[MIT](LICENSE)
