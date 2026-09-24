# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/).

## [0.1.2] - 2026-09-24

### Added

- 新增站点落地页 `index.md`：按量潮数据、量潮课堂、量潮云、量潮咨询的顺序介绍四条业务线
- 新增四条业务线的案例总览：`qtdata/index.md`（采集／清洗／大模型挖掘）、`qtclass/index.md`（校企合作／社会招生）、`qtcloud/index.md`（SaaS／PaaS）、`qtconsult/index.md`（创业咨询／创新咨询）
- 新增仓库文档套件 `AGENTS.md`、`CONTRIBUTING.md`、`STATUS.md`、`ROADMAP.md`

### Changed

- `myst.yml`：目录按业务线分组（数据、课堂、云、咨询），首项改为 `index.md`，并开启 `site.options.folders`
- `README.md`：由标题改写为仓库说明，含结构、本地构建与发布方式
- 量潮数据案例总览的分类由「采集／清洗／精炼」改为「采集／清洗／大模型挖掘」

### Fixed

- CI 补 `BASE_URL`：此前构建产出的资源路径与站内链接为根路径，在 GitHub Pages 项目站下全部 404
- 产品页 URL 由兜底 slug（`/index-1` 等）恢复为 `/qtdata`、`/qtclass`、`/qtcloud`、`/qtconsult`

## [0.1.1] - 2026-08-27

### Changed

- 整理 qtclass 文档格式，vibe_coding 重命名为 vibe-coding
- 更新 myst.yml，添加 toc 配置

### Removed

- 删除 connect、docs、devops、mkt、execute、infra、read、think、write 目录
- 删除 agent/prompts 目录

### Moved

- qtdata 迁移至归档站（data/archive/gallery/qtdata）
- vibe-coding.md 迁移至归档站（data/archive/gallery/qtclass/vibe-coding.md）

## [0.1.0] - 2026-05-05

### Changed

- 重构：日期命名的日志文件统一改为 journal.md
- 新增 write/report.md 工作报告

## [0.0.4] - 2026-04-11

### Added
- 新增文档格式技能
- 新增 md 格式触发

### Changed
- 重命名技能目录为领域-技能格式
- 补充格式技能内容
- 添加检查文档格式触发
- 添加使用时机到 description
- 按 release.md 规范重写 release 技能
- 扩充版本号为验收标准并明确验收方式
- 将版本号规则移至附录

## [0.0.3] - 2026-04-11

### Changed
- 按 release.md 规范重写 release 技能
- 扩充版本号为验收标准并明确验收方式
- 将版本号规则移至附录

## [0.0.2] - 2026-04-11

### Added
- 新增 agent 提示词案例（8个提示词文件）

### Changed
- 中文化 README 标题

## [0.0.1] - 2026-04-02

### Added

- 初始版本
- 企业实体案例展示框架
- 职能板块目录结构（connect、execute、think、write）
