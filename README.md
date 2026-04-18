# ANTHROPIC — Claude 系统提示词档案库

本仓库收集并整理了 Anthropic 旗下 Claude 系列模型在不同时期、不同产品形态下使用的 **系统提示词（System Prompts）**，以及与 Claude 生态相关的内部指令文档（如 Claude Code、Claude Design、UserStyle 模式等）。

档案按照模型版本和发布时间进行组织，方便研究者、提示词工程师以及对大型语言模型行为机制感兴趣的开发者查阅、对比和分析 Claude 在不同迭代中的能力边界、安全策略、行为准则与工具使用约定的演进。

---

## 仓库内容

### 模型系统提示词

| 文件名 | 对应模型 | 参考日期 | 说明 |
| --- | --- | --- | --- |
| `Claude_Sonnet_3.5.md` | Claude 3.5 Sonnet | 2024-06-20 | Claude 3 家族，包含 `claude_info`、`claude_image_specific_info`、`claude_3_family_info`、早期 Artifacts 规范 |
| `Claude_Sonnet_3.7_New.txt` | Claude 3.7 Sonnet | 2025-05-16 | 引入 web_search 工具的使用规范与扩展的核心身份描述 |
| `Claude_4.txt` | Claude Sonnet 4 | 2025-05-22 | Claude 4 家族首批版本，模型字符串 `claude-sonnet-4-20250514` |
| `Claude-4.1.txt` | Claude 4.1 | 2025-08-05 | 完整还原尝试版，包含 citation_instructions、artifacts_info 等完整分区 |
| `Claude-4.5-Opus.txt` | Claude 4.5 Opus | — | 使用 `{antml:cite}` 占位符的模板化系统提示词 |
| `Claude_Sonnet-4.5_Sep-29-2025.txt` | Claude Sonnet 4.5 | 2025-09-29 | 知识截止 2025 年 1 月，含图像处理与引用规范 |
| `Claude_Opus_4.6.txt` | Claude Opus 4.6 | 2026-02-06 | 引入 `<computer_use>`、`<skills>` 等新能力说明 |
| `Claude-Opus-4.7.txt` | Claude Opus 4.7 | — | 目前公开最先进的模型版本，强调 `search_first` 原则 |

### Claude 生态相关指令

| 文件名 | 内容 | 说明 |
| --- | --- | --- |
| `Claude_Code_03-04-24.md` | Claude Code CLI 系统指令 | Anthropic 官方命令行工具的系统提示词 |
| `Claude-Design-Sys-Prompt.txt` | Claude 设计模式提示词 | 面向 HTML 设计产出（UX、幻灯片、原型、动画等）的专家角色定义 |
| `UserStyle_Modes.md` | Anthropic 三种用户样式 | Explanatory（讲解）/ Formal（正式）/ Concise（简洁）模式完整定义 |

---

## 使用场景

这份档案可以用于以下几类工作：

**提示词研究与对比**  
通过纵向对比 Claude 3.5 → 4 → 4.7 的系统提示词，可以追踪 Anthropic 在引用规范、工具调用、安全策略、人格设定、拒答策略等方面的迭代轨迹。

**产品形态差异分析**  
对比聊天界面（claude.ai）、Claude Code、Claude Design、Cowork 等不同产品下的系统提示词，理解同一模型如何针对不同使用场景进行"人格化塑形"。

**行为机制学习**  
阅读 Claude 关于 Artifacts、computer_use、skills、web_search、file_creation 等能力的原始指令，对于从事 Agent 框架开发、提示词工程、模型对齐研究等方向的工程师具有直接参考价值。

**用户样式（UserStyle）参考**  
`UserStyle_Modes.md` 中的三种模式可以直接用作自定义 AI 助手的写作风格模板。

---

## 目录结构

```
ANTHROPIC/
├── README.md                              # 本文件
├── Claude_Sonnet_3.5.md                   # Claude 3.5 Sonnet 系统提示词
├── Claude_Sonnet_3.7_New.txt              # Claude 3.7 Sonnet 系统提示词
├── Claude_4.txt                           # Claude Sonnet 4 系统提示词
├── Claude-4.1.txt                         # Claude 4.1 系统提示词（完整版）
├── Claude-4.5-Opus.txt                    # Claude 4.5 Opus 模板化系统提示词
├── Claude_Sonnet-4.5_Sep-29-2025.txt      # Claude Sonnet 4.5 系统提示词
├── Claude_Opus_4.6.txt                    # Claude Opus 4.6 系统提示词
├── Claude-Opus-4.7.txt                    # Claude Opus 4.7 系统提示词
├── Claude_Code_03-04-24.md                # Claude Code CLI 系统指令
├── Claude-Design-Sys-Prompt.txt           # Claude 设计模式提示词
└── UserStyle_Modes.md                     # Anthropic 用户样式三模式
```

---

## 版本时间线

以下列表按照每个文件内记录的"当前日期"排序，便于理解 Claude 系统提示词的演进轨迹：

1. **2024-06-20** — Claude 3.5 Sonnet
2. **2024-03-04** — Claude Code（早期 CLI 指令）
3. **2025-05-16** — Claude 3.7 Sonnet
4. **2025-05-22** — Claude Sonnet 4
5. **2025-08-05** — Claude 4.1
6. **2025-09-29** — Claude Sonnet 4.5
7. **2026-02-06** — Claude Opus 4.6
8. **—** — Claude 4.5 Opus / Claude Opus 4.7（无明确日期标记）

---

## 阅读建议

第一次接触这批文档的读者，建议按以下顺序阅读：

先阅读 `Claude_Sonnet_3.5.md`，了解 Claude 早期相对简洁的提示词结构。然后跳到 `Claude-4.1.txt`，它是结构最清晰、分区最完整的版本，能够帮助理解每个 XML 分区（citation_instructions、artifacts_info、search_instructions、refusal_handling 等）的作用。随后再看 `Claude-Opus-4.7.txt` 和 `Claude_Opus_4.6.txt`，理解 Anthropic 如何在最新模型中引入 computer_use、skills、Cowork 等新能力。最后可以查阅 `Claude_Code_03-04-24.md` 与 `Claude-Design-Sys-Prompt.txt`，感受同一模型在不同产品线下的人格差异。

---

## 免责声明

本仓库收集的系统提示词内容均来源于公开渠道流出或社区还原，**并非 Anthropic 官方发布的权威文本**。文件中可能存在不完整、部分还原或版本拼接的情况。仓库仅用于学习、研究和提示词工程实践，不代表 Anthropic 的官方立场，也不应被视为可用于商用部署的规范文档。

如需 Anthropic 官方信息，请访问：

- 官方网站：<https://www.anthropic.com>
- 官方文档：<https://docs.claude.com>
- 帮助中心：<https://support.claude.com>

---

## 贡献

若您发现文档中存在错误、版本混淆，或手头持有更完整、更新的 Claude 系统提示词副本，欢迎通过 Pull Request 的方式进行补充和修正。建议提交时：

在文件名中明确标注模型版本与日期（例如 `Claude_Opus_4.8_2026-XX-XX.txt`）。保留原始文本的分区、缩进与 XML 结构，避免二次改写。若内容为部分还原，请在文件顶部以注释或说明形式标注"Partial / Reconstructed"。
