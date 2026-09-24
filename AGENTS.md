# AGENTS.md

本仓库是量潮科技工作案例库（`quanttide-gallery-of-business-entity`），是 `quanttide-tech` 的子模块（`docs/gallery`）。案例是写给人看的——潜在客户、合作方、应聘者——不是内部归档。

## 工作流程

新增或修改案例，按这个顺序走：

1. 读[案例编写规范](CONTRIBUTING.md)与[文档格式标准](https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/docs/format.md)。
2. 到各内容仓库找这条业务的**对外口径**（`data/brochure/`、`docs/tutorial/`、`docs/essay/`、`docs/handbook/` 各存一份，口径不一），以创始人给的原始说法为准。
3. 写进对应业务线目录的 `index.md`。
4. 本地构建通过：`BASE_URL=/quanttide-gallery-of-business-entity myst build --html`。
5. 在子模块内提交推送，然后回 `quanttide-tech` 更新 `docs/gallery` 指针。

## 三条硬规矩

- **价格不写进案例**。报价倍数、客单价、订阅方案一律不写——那是商务信息，留在 `data/brochure/` 与业务档案里。
- **客户不点名**。写「某高校研究者」「某制衣厂」；已公开的口径除外（如浙江理工大学计算机系的校企合作已在课程材料中公开）。
- **未完成的如实说**。内测、未标准化的产品要写明状态（例：量潮 DevOps 云命令行工具写明 v0.4.x 内测、公开它是作为课堂案例和笔试题、不建议生产使用）。

## 结构规则

- 一个业务线一个目录，目录内一个 `index.md` 作入口，具体案例作为同目录下的文件挂在它后面。
- `myst.yml` 的 toc 按业务线分组，顺序固定为：量潮数据 → 量潮课堂 → 量潮云 → 量潮咨询。
- `site.options.folders` 必须为 `true`，否则产品页 URL 会退化成 `index-1`、`index-2` 这种兜底 slug。
- toc 首项是 `index.md`（站点落地页），`README.md` 只作仓库说明、不进 toc。

## 工程标准规范

遵循量潮科技工程标准规范（v0.1.1）：

- 文档格式标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/docs/format.md
- 版本发布标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md
- Git 使用标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/git.md
- Git 仓库标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/asset/type/git_repo.md

## 首要范例

`qtdata/index.md` 是案例页范例：先一句业务定位，再按业务的真实分类分节，每节给具体做法与真实数字，不铺陈、不写价格与客户名。

## 相关文档

[CONTRIBUTING](CONTRIBUTING.md)、[README](README.md)、[STATUS](STATUS.md)、[ROADMAP](ROADMAP.md)
