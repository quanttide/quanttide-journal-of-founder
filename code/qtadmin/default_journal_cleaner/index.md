# Journal Cleaner - 工作日志清洗器

自动将原始工作日志转换为结构化的事件记忆和清洗后的日记。

## 概述

- **目标**：从原始工作日志中提取事件记忆
- **输入**：`default/raw/YYYY-MM-DD_N.md`
- **输出**：
  - 清洗后日记：`default/journal/diary/YYYY-MM-DD.md`
  - 事件记忆：`default/memory/episodic/YYYY-MM-DD.jsonl`

## 配置

- 模型：DeepSeek（默认）
- 知识库根路径：`.env` 中的 `KNOWLEDGE_BASE_ROOT`
- 批量处理：一次性处理所有文件
- 重试次数：3 次

## 相关文档

- [清洗](./clean.md)：将原始日志清洗为可读日记
- [提炼](./refine.md)：从原始日志提取事件记忆
