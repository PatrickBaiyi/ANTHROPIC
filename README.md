# ANTHROPIC

这是一个收集 Claude 各版本 system prompt 与相关说明文本的资料仓库，内容以阅读、对比、归档和研究为主，不是可运行项目。

## 仓库概览

当前仓库为扁平结构，主要包含以下几类内容：

- Claude 不同版本的 system prompt 文本
- 特定用途的 prompt（如设计场景）
- Claude Code 的说明文档
- UserStyle 模式定义文档

从已收录文件看，内容覆盖了 Claude 3.5 Sonnet、Claude 3.7 Sonnet、Claude Sonnet 4、Claude Sonnet 4.5，以及 Claude Opus 4.6 / 4.7 等版本或相关变体。

## 文件清单

| 文件名 | 类型 / 主题 | 简述 |
| --- | --- | --- |
| `Claude_Sonnet_3.5.md` | Claude 3.5 Sonnet | 较早期的 Claude 3.5 Sonnet system prompt 文本，包含 artifacts 相关说明。 |
| `Claude_Sonnet_3.7_New.txt` | Claude 3.7 Sonnet | Claude 3.7 Sonnet 的 system prompt，包含模型信息、产品说明与行为约束。 |
| `Claude_4.txt` | Claude Sonnet 4 | Claude Sonnet 4 的 system prompt，包含产品信息、提示工程建议与安全边界。 |
| `Claude-4.1.txt` | Claude 相关 prompt 变体 | 文件名为 4.1，但开头内容更像一份带有 citation 与 artifacts 分区的完整 prompt 重建文本。 |
| `Claude-4.5-Opus.txt` | Claude 4.5 / Opus 相关 prompt | 包含 citation instructions、search-first 与产品信息等规则。 |
| `Claude_Sonnet-4.5_Sep-29-2025.txt` | Claude Sonnet 4.5 | Claude Sonnet 4.5 的 prompt 文本，含图像限制、citation 与 past chats 相关说明。 |
| `Claude_Opus_4.6.txt` | Claude Opus 4.6 | Claude Opus 4.6 的 prompt 文本，含 skills、文件创建建议与工具使用约束。 |
| `Claude-Opus-4.7.txt` | Claude Opus 4.7 | Claude Opus 4.7 的 prompt 文本，包含较新的产品信息与默认行为设定。 |
| `Claude-Design-Sys-Prompt.txt` | 设计专项 prompt | 面向 HTML 设计产出的专项系统提示词，强调设计工作流与交付要求。 |
| `Claude_Code_03-04-24.md` | Claude Code | Claude Code CLI 的早期系统说明，涵盖安全规则、slash commands、记忆与风格约束。 |
| `UserStyle_Modes.md` | UserStyle 模式 | 定义 Explanatory、Formal、Concise 三种输出风格。 |

## 主要内容主题

根据当前文件内容，这个仓库主要涵盖以下主题：

- 模型身份、版本信息与 Anthropic 产品说明
- web search、citation、past chats 等使用规则
- artifacts 的使用边界与输出约束
- 安全、合规与拒绝策略
- Claude Code CLI 的行为规范
- 用户输出风格模式（Explanatory / Formal / Concise）

## 如何使用

这个仓库无需安装依赖，也没有构建或运行步骤。可直接按文件名阅读，或横向对比不同版本 prompt 在以下方面的变化：

- 模型定位与产品描述
- 搜索与引用规范
- 工具使用约束
- 安全策略与风格设定

如果你是为了做资料整理或提示词演化分析，建议先从 `Claude_Sonnet_3.5.md`、`Claude_4.txt`、`Claude_Opus_4.6.txt`、`Claude-Opus-4.7.txt` 这几份文件开始阅读。

## 说明

本仓库中的文件为收集整理的 prompt 文本资料，仅供学习与参考使用；其中内容的准确性、完整性与来源背景请自行甄别。

## 备注

- 仓库当前没有代码、依赖配置或可执行入口。
- README 中的摘要仅基于现有文件可直接观察到的内容整理，尽量避免对来源和版本关系作额外推断。
- 若后续新增文件，建议继续按“文件名 + 类型/主题 + 简述”的方式补充到清单中。
