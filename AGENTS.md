# AGENTS.md

本仓库是量潮科技工作案例库（`quanttide-gallery-of-business-entity`），是 `quanttide-tech` 的子模块（`docs/gallery`）。案例是写给人看的——潜在客户、合作方、应聘者——不是内部归档。贡献细则、案例编写规范与工程标准清单见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 工作流程

新增或修改案例，按这个顺序走：

1. 读 [CONTRIBUTING.md](CONTRIBUTING.md) 的案例编写规范与文档格式标准。
2. 到各内容仓库找这条业务的对外口径（`data/brochure/`、`docs/tutorial/`、`docs/essay/`、`docs/handbook/` 各存一份，口径不一），以创始人给的原始说法为准。
3. 写进对应业务线目录：`qtdata/` 按服务类别子目录放（如采集案例进 `qtdata/collection/`），其余业务线挂入口 `index.md` 后面；新增文件同步加进 `myst.yml` 的 toc。
4. 本地构建通过：`BASE_URL=/quanttide-gallery-of-business-entity myst build --html`。
5. 在子模块内提交推送，然后回 `quanttide-tech` 更新 `docs/gallery` 指针。

## 不可违反

口径红线（详见 [CONTRIBUTING.md](CONTRIBUTING.md)）：

- 价格不写进案例。
- 客户不点名，已公开口径除外。
- 未完成的产品如实说明状态。

站点不变量（破坏任何一个都会让线上站出问题）：

- `site.options.folders` 必须为 `true`，否则产品页 URL 退化成 `index-1` 这种兜底 slug。
- toc 首项必须是 `index.md`，顺序固定为：量潮数据 → 量潮课堂 → 量潮云 → 量潮咨询；`README.md` 不进 toc。
- 构建必须带 `BASE_URL=/quanttide-gallery-of-business-entity`，否则发到 GitHub Pages 后资源与站内链接全部 404。

## 首要范例

`qtdata/index.md` 是案例页范例：先一句业务定位，再按业务的真实分类分节，每节给具体做法与真实数字，不铺陈、不写价格与客户名。

## 相关文档

[CONTRIBUTING](CONTRIBUTING.md)、[README](README.md)、[STATUS](STATUS.md)、[ROADMAP](ROADMAP.md)
