# gold-finance-logic

以黄金为锚的金融底层逻辑学习框架，既是一份可交互学习网页，也是一套可安装到 WorkBuddy 的 Skill。

## 直接体验

打开在线交互页：

<https://zhaangzee.github.io/zhaangzee-215ing/>

网页包含：

- 6 个学习模块：黄金属性、四层传导、三条底层链、五大反转、三个宏观案例、实战七步。
- 18 道基础自测，答错后提供解析与相似题重测。
- 浏览器本地进度保存。
- 判断句生成器与情景矩阵。

## 这个 Skill 能做什么

- 用金融底层逻辑分析财经事件。
- 按课程口径生成学习材料与自测题。
- 在用户答错后生成结构相同、措辞不同的相似题。
- 把判断整理成可检验的完整句子。

## 安装

从仓库根目录执行：

```bash
mkdir -p "$HOME/.workbuddy/skills"
cp -r gold-finance-logic "$HOME/.workbuddy/skills/gold-finance-logic"
```

Windows PowerShell：

```powershell
New-Item -ItemType Directory -Force "$HOME\.workbuddy\skills" | Out-Null
Copy-Item -Recurse -Force ".\gold-finance-logic" "$HOME\.workbuddy\skills\gold-finance-logic"
```

## 目录

| 文件 | 用途 |
| --- | --- |
| `SKILL.md` | Skill 元信息、触发条件与工作流 |
| `references/finance_logic.md` | 完整知识底稿与内容口径 |
| `assets/finance-logic-framework.html` | 可交互学习网页 |

## 内容底线

**黄金价格 = 机会成本 + 保险价值**。中短期看实际利率与美元，长周期看信用风险与央行购金。所有宏观指标都只是改变预期的入口，不是价格的直接原因。

> 本目录内容仅用于金融认知学习，不构成投资建议。

[返回项目主页](../README.md)
