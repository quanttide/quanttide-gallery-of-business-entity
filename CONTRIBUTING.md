# 贡献指南

本仓库是量潮科技工作案例库，案例是写给人看的——潜在客户、合作方、应聘者——不是内部归档。贡献方式：报告问题通过 GitHub Issues，提交修改通过 Pull Request。

## 提交流程

本仓库是 `quanttide-tech` 的子模块，改完要逐层回到父仓库：

1. 子模块内提交推送：`git commit -m "docs: …"`、`git push`
2. 更新父仓库指针：在 `quanttide-tech` 里 `git add docs/gallery && git commit -m "chore: update gallery submodule"`、`git push`
3. 若父仓库也在根仓库的子模块里，再更新 `quanttide` 的 `default/quanttide-tech` 指针

提交信息用 Conventional Commits（`docs:` / `fix:` / `chore:`）。

## 案例编写规范

### 组织方式

一个业务线一个目录，目录内一个 `index.md` 作入口，具体案例作为同目录下的文件挂在它后面。新增案例文件时同步加进 `myst.yml` 的 toc。

`qtdata/` 在业务线目录下再按服务类别分子目录。采集、清洗、精炼是量潮数据定义的三种主要服务类别（`collection/` = 采集），案例归到哪一类看项目重心落在哪类服务（例：法规情报中心重心在采集，归入 `collection/`）。案例库的重点不在于某个具体需求，而在于通过案例建立某类项目的完整规范——所以按服务类别组织目录、用类别名命名，而不是按需求主题给文件命名。类别子目录的 `index.md` 承载该类项目的规范正文，业务线 `index.md` 只留摘要并链接过去。

一个案例页回答三件事：这条业务是什么、它分哪几类、每一类里我们实际怎么做（给真实做法与数字）。分类要跟业务的真实交付方式走，不要套统一模板——量潮数据按服务类别分（采集／清洗／精炼）、量潮课堂按招生方式分（校企合作／社会招生）、量潮云按产品形态分（SaaS／PaaS）、量潮咨询按客户类型分（创业／创新）。

### 取材与口径

取材以创始人给的原始说法为准。各内容仓库里同一条业务有多个版本（宣传册偏客户视角、手册偏操作、随笔偏主张），写案例时取宣传册与教程的对外口径，把内部分析语汇压回去。

口径上守三条，宁少而准——案例不是文章，是口径，谁读都不会误解我们在卖什么：

- 价格不写进案例。报价倍数、客单价、订阅方案一律不写，那是商务信息，留在 `data/brochure/` 与业务档案里。
- 客户不点名。写「某高校研究者」「某制衣厂」；已公开的口径除外，如浙江理工大学计算机系的校企合作已在课程材料中公开。
- 未完成的如实说。内测、未标准化的产品要写明状态，例：量潮 DevOps 云命令行工具写明 v0.4.x 内测、公开它是作为课堂案例和笔试题、不建议生产使用。

### 站点结构

`myst.yml` 的 toc 按业务线分组，顺序固定为：量潮数据 → 量潮课堂 → 量潮云 → 量潮咨询。toc 首项是 `index.md`（站点落地页），`README.md` 只作仓库说明、不进 toc。

`site.options.folders` 必须为 `true`，否则产品页 URL 会退化成 `index-1`、`index-2` 这种兜底 slug。

## 编写规范

遵循量潮科技文档格式标准：删除不必要的格式元素，优先用段落和标题；能用列表就不表格，能用文字就不列表；同一概念全程使用相同名称。

提交前对照格式规范检查一遍：加粗是否过度（列表项内、连续多个、标记所有术语）；列表是否滥用（简单对应关系、可段落化的内容）；标题层级是否过深（四级及以上）；引号是否用中文引号。改完跑一次构建，确认通过、站内链接没断：

```bash
BASE_URL=/quanttide-gallery-of-business-entity myst build --html
```

`BASE_URL` 不能省：省掉时产物里的资源路径与站内链接都是根路径，本地能看，发到 GitHub Pages 项目站会全部 404。

## 工程标准

遵循量潮科技工程标准规范（v0.1.1）：

- 文档格式标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/docs/format.md
- 版本发布标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md
- Git 使用标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/git.md
- Git 仓库标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/asset/type/git_repo.md
