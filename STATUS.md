# STATUS

仓库当前快照，供 Agent 与协作者快速了解现状。快照有时效，以最新提交为准；维护流程见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

> 快照日期：2026-09-24（v0.1.2 之后）

## 站点现状

线上站点已修复并可正常使用：CI 补上 `BASE_URL` 后资源与站内链接恢复 200，`myst.yml` 开启 `folders` 后产品页 URL 为 `/qtdata`、`/qtclass`、`/qtcloud`、`/qtconsult`，不再是 `index-1` 这类兜底 slug。

内容共 7 个页面：落地页、四条业务线入口、两个具体案例（采集案例·全球法规情报中心、大数据导论实践课任务书）。四个业务线目录各有 `index.md`，其中 `qtdata/` 已按服务类别建子目录（`collection/` 为采集）。

口径已立住：四个入口页取自 brochure、tutorial、handbook 的对外版本，价格与客户名未上站，量潮数据的三类服务统一为「采集／清洗／精炼」。

## 待补

量潮云与量潮咨询两条业务线只有入口介绍，还没有能拿出去看的完整案例，这是当前最大的缺口。案例与归档站的分工目前只在 README 里一句话带过，未写成规则。CI 只有构建与部署，没有链接检查与格式检查；仓库没有 `.gitignore`，`_build/` 要手工清理。自有域名 `gallery.quanttide.com` 未解析，仍在 github.io 项目地址上。

具体排期见 [ROADMAP.md](./ROADMAP.md)。

## 已知不一致

`quanttide-tech` 的 CONTRIBUTING 里仍写着「稳定的 SKILL 可同步到 gallery 仓库」，指向本仓库并不存在的 `devops/` 目录。本仓库定位是业务案例库，该条属于 tech 仓库，需在那边改。

历史上内容持续迁出（`qtdata/` 目录、`agent/prompts/` 等先后删除迁往归档站），迁移规则至今未成文。
