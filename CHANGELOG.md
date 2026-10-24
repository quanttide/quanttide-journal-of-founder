# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### 变更

- `media/` 域目录更名为 `create/`：`media/2026-10/2026-10-16.md` → `create/2026-10/2026-10-16.md`（纯路径迁移，内容不变）

## [1.0.1] - 2026-10-24

### 新增

- 迁入 `data/context/{default,life,work,write}/journal/` 的 21 篇日志（2026-10-17 ~ 2026-10-23），按域与月份分二级目录；`life/` 为新增域目录
- 迁入 `data/context/{default,media,work,write}/journal/` 的 11 篇日志（2026-10-13 ~ 2026-10-16），按域与月份分二级目录；`media/` 为新增域目录
- 迁入 `data/context/think/journal/` 的 2 篇日志（2026-10-17 ~ 2026-10-18），按月份分二级目录 `think/<YYYY-MM>/`；`think/` 为新增域目录

## [1.0.0] - 2026-10-13

### 新增

- 仓库初始化：`README.md`、`CONTRIBUTING.md`（日志贡献指南）、`default/` 入口与 `CHANGELOG.md`
- 迁入 `data/archive/journal/default/` 的 183 篇日志（2026-03-11 ~ 2026-09-19），按月份分二级目录 `default/<YYYY-MM>/`
- 迁入 `data/context/default/journal/` 的 23 篇日志（2026-09-20 ~ 2026-10-12），按月份分二级目录 `default/<YYYY-MM>/`
- 迁入 `data/context/fiction/journal/` 的 21 篇创作日志（2026-09-05 ~ 2026-10-11），按月份分二级目录 `write/<YYYY-MM>/`
- 迁入 `data/archive/fiction/journal/` 的 4 篇创作日志（2026-03-16 ~ 2026-03-31），按月份分二级目录 `write/<YYYY-MM>/`
- 迁入 `data/context/work/journal/` 的 10 篇工作日志（2026-10-03 ~ 2026-10-12），按月份分二级目录 `work/<YYYY-MM>/`

### 变更

- 命名规则增加月份二级目录：`<域>/<YYYY-MM>/YYYY-MM-DD.md`
