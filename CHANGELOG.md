# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/).

## [Unreleased]

## [0.2.2] - 2026-11-12

### Added

- 产品分层案例 `qtadmin/product/layer.md`：领域层是模块化能力单元（沟通云、人事云），应用层对应实际业务需求（量潮课堂），量潮云是领域层大集成的应用层，注册进 `myst.yml` toc
- 众包复用案例 `qtclass/crowd.md`：课堂实践体系复用众包管理模块的上线流程（quanttide-crowd 更新 profile → AI 上线 qtclass → lite 发新 patch）与合规留痕，注册进 `myst.yml` toc
- 资产案例 `qtadmin/asset/gallery.md`：公司 gallery 是领域 gallery 的精简版，领域 gallery 是最终事实源，注册进 `myst.yml` toc

### Changed

- `qtadmin/product/scope.md` 容器范围补充 studio（付费客户管理用户的学习进度）与访问链路：进来先看 site，用户从 site 根据需要进入 lite，付费客户进入 studio，该模式对量潮所有平台成立
- `qtadmin/product/method.md` 落地流程补充 UX 优先：UI 先不管、能用即可，最后所有 APP 一起统一；新增真实需求：实训基地是课堂的养料，做出来的就是真实软件
- `qtadmin/product/role.md` 产品策划协作补充：快速反应、面对一线需求，把发现的问题转化成产品
- `qtadmin/index.md` 入口页登记产品分层与资产板块，组织板块移除部门链接
- `qtclass/index.md` 登记众包板块，移除失效的任务书链接

### Removed

- `qtadmin/org/department.md` 整体迁往 quanttide-org 领域 gallery（`docs/gallery/department/index.md`），toc 同步移除
- `qtclass/big-data-practice.md` 过时任务书，已上架 quanttide-course 领域 gallery（`docs/gallery/course/index.md`），toc 同步移除

## [0.2.1] - 2026-11-12

### Added

- 绩效案例 `qtadmin/human/performance.md`：证明材料与推荐信分层发放、先例约束、退出衔接，注册进 `myst.yml` toc 与入口页
- 议事规则案例 `qtadmin/delib/rule.md`：公司与联盟两级认证、制衡机制、立法信息反馈，新增议事域，注册进 `myst.yml` toc 与入口页
- 产品方法案例 `qtadmin/product/method.md`：落地流程（原型软件不限制、团队层面交付 HTML）与调研先行，注册进 `myst.yml` toc 与入口页
- 产品范围案例 `qtadmin/product/scope.md`：site 与 lite 容器分工——site 介绍规则、基本不接入服务器，lite 提供信息、动态变化，注册进 `myst.yml` toc 与入口页

### Changed

- `qtadmin/connect/group.md` 选群新增私下讨论：不便创始人在场的讨论用秘书处办公室等没有创始人的群
- `qtadmin/product/role.md` 产品策划新增协作方式：idea 由策划提供，容器由创始人指定或自行判断列出
- `qtadmin/org/duty.md` 新增 CEO 助理职责：需要创始人账号操作的事务由助理扫码登录代操作

## [0.2.0] - 2026-11-11

### Added

- 量潮管理后台职能案例 8 篇：群聊、会议（connect），培训、员工关系（human），部门、职位、职级（org），角色（product），并注册进 `myst.yml` toc
- 量潮管理后台入口页 `qtadmin/index.md`：按组织／人力／沟通／产品四个职能域汇总上述页面
- 站点落地页 `index.md` 新增「量潮管理后台」一节
- `myst.yml` toc 新增「量潮管理后台」分组，qtadmin 各页面由散挂收进组内
- 职责案例 `qtadmin/org/duty.md`：创始人职能从日常经营（行政权）与制度建设（立法权）转向梳理制度与编制法典（司法权），明确两个工作方案（CEO办公室群梳理编制案例、大群解释固化制度）及各自的执行安排，并注册进 `myst.yml` toc 与入口页

### Changed

- `qtadmin/connect/group.md` 重组为二级标题「选群」（就地讨论、岔题转群）与「自媒体文章链接」（创始人个人／创始人工作／公司工作三层级提醒渠道）

### Removed

- 删除采集案例「全球法规情报中心」（`qtdata/collection/`），量潮数据入口页同步移除该案例段落，`myst.yml` toc 同步移除
- 删除仓库文档 `STATUS.md`、`ROADMAP.md`、`CONTRIBUTING.md`、`AGENTS.md`，`README.md` 文档列表与站内链接同步清理

## [0.1.3] - 2026-09-24

### Added

- 具体案例「全球法规情报中心」（`qtdata/collection/index.md`），数据线首个按服务类别建立的案例
- `.gitignore`：排除 `_build/` 等本地构建产物

### Changed

- 量潮数据的第三类服务由「大模型挖掘」统一改回「精炼」，与服务类别定义（采集／清洗／精炼）及对外口径一致
- 法规情报案例由 `qtdata/regulatory-intelligence.md` 迁至 `qtdata/collection/index.md`，qtdata 开始按服务类别建子目录
- 重写 README、STATUS、ROADMAP、AGENTS、CONTRIBUTING：格式对齐文档格式标准，内容分层——细则归 CONTRIBUTING，AGENTS 只留工作流程、口径红线与站点不变量

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
