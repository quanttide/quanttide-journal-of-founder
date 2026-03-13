# CHANGELOG

## [Unreleased]

## [0.1.1] - 2026-03-14

### 新增

- 新增事件记忆提取流程：将原始日志转换为事件记忆和日记
- 新增 memory/event/ 目录：存储事件记忆 JSONL 文件
- 新增 journal/diary/ 目录：存储整理后的日记
- 新增 raw/archive/ 目录：归档已处理的原始日志

### 优化

- 完善工作日志处理流程
- 建立事件提取和日记整理的标准化方法

## [0.1.0] - 2026-03-13

### 初始化

- 初始化 journal 子模块
- 新增 AGENTS.md：Agent 工作指南
- 新增 .gitignore：环境变量和 Python 缓存
- 新增 .env.example：环境变量模板
- 新增 README.md：日志分类说明
