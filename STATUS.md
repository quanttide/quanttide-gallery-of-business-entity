# 状态：工作案例库对照规范

体检日 2026-09-24（四条业务线入口页与发布链修好之后）。本仓库没有专属契约，尺子取三处：家族内容仓库的文档套件（handbook、tutorial 为范例）、量潮科技工程标准规范（v0.1.1）、`quanttide-tech` 的 CONTRIBUTING 里对本仓库的约定。

## 规模

| 项 | 数 |
|---|---|
| 跟踪文件 | 15（含 .github、LICENSE、myst.yml） |
| 站点页面 | 7：落地页 + 四条业务线入口 + 2 个具体案例（大数据导论实践课任务书、全球法规情报中心） |
| 内容目录 | 4：`qtdata/`、`qtclass/`、`qtcloud/`、`qtconsult/`，每个内一个 `index.md` |
| 线上站点 | https://quanttide.github.io/quanttide-gallery-of-business-entity/ |
| 最近版本 | v0.1.2（2026-09-24） |

## 对照

| 条款 | 现状 | 判定 |
|---|---|---|
| 文档套件齐全（AGENTS／CONTRIBUTING／README／ROADMAP／CHANGELOG） | 原本只有 README、CHANGELOG、index；2026-09-24 补齐 AGENTS、CONTRIBUTING、ROADMAP、STATUS | ✓ |
| 一条业务线一个目录、目录内 `index.md` 作入口 | 四个目录都有 `index.md`，与本家族（handbook／tutorial／brochure）一致 | ✓ |
| toc 分组与站点结构一致 | toc 按业务线分组，顺序为数据 → 课堂 → 云 → 咨询 | ✓ |
| 站点资源与站内链接可用 | 曾因缺 `BASE_URL` 导致线上 CSS／JS 与站内链接全部 404（站是坏的）；产品页 URL 曾是 `index-1` 兜底 slug。2026-09-24 补 `BASE_URL` 与 `site.options.folders` 后修复，实测资源与四条链接均 200 | ✓ 已修 |
| 案例取材于各内容仓库的对外口径 | 四个入口页分别取自 brochure／tutorial／handbook 的对外版本，价格倍数与客户名未上站 | ✓ |
| 具体案例覆盖四条业务线 | 数据线有 1 个（全球法规情报中心）、课堂线有 1 个（大数据导论实践课任务书）；云、咨询两条仍只有入口介绍 | ✗ 待补 |
| 案例与归档站的分工成文 | 交付原件在 `quanttide-archive-of-business-entity`，本仓库只留介绍与主张——目前只在 README 里一句带过 | ⚠ 待写实 |
| 自有域名 | 走 `github.io` 项目地址，`gallery.quanttide.com` 未解析 | ✗ 未接 |
| 格式校验门禁 | CI 只 `myst build` + 部署，无链接检查、无格式检查 | ✗ 缺 |

## 已知不一致

1. `quanttide-tech` 的 CONTRIBUTING 里仍写着「稳定的 SKILL 可同步到 gallery 仓库：`cp .agents/skills/<skill>/SKILL.md docs/gallery/devops/<skill>/SKILL.md`」——本仓库现在没有 `devops/` 目录，那条流程从未跑过；本仓库的实际定位是业务案例库。该条属于 tech 仓库，需在那边改。
2. 历史上内容持续迁出（`qtdata/` 目录、`agent/prompts/`、`execute/infra/read/think/write/` 等先后删除，迁往归档站），但迁移规则未成文。
3. README 与 index.md 曾共用一个文件（都只有一行标题），现已分工：README 作仓库说明、index.md 作站点落地页。

## 一句话

工作案例库现在是**「四条业务线的介绍 + 每两条业务线一个具体案例」**：入口齐了、站修好了、口径立住了，欠的是内容——云与咨询两条业务线下还没有能拿出去看的完整案例。
