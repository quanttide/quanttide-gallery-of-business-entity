# 量潮科技工作案例

量潮科技四条业务线（量潮数据、量潮课堂、量潮云、量潮咨询）的公开工作案例，写给潜在客户、合作方与应聘者看。

在线阅读：https://quanttide.github.io/quanttide-gallery-of-business-entity/

本仓库只留案例的介绍与主张；案例的交付原件（需求范围、报价、蓝图、交付物）在归档站 `quanttide-archive-of-business-entity`。

## 仓库结构

```
index.md                       站点落地页：四条业务线的简表
qtdata/index.md                量潮数据入口（采集／清洗／精炼）
qtdata/collection/index.md     采集案例：全球法规情报中心
qtclass/index.md               量潮课堂入口（校企合作／社会招生）
qtclass/big-data-practice.md   案例：大数据导论实践课任务书
qtcloud/index.md               量潮云入口（SaaS／PaaS）
qtconsult/index.md             量潮咨询入口（创业咨询／创新咨询）
myst.yml                       MyST 站点配置（toc 与主题）
```

仓库文档：[AGENTS](AGENTS.md)（Agent 工作规则）、[CONTRIBUTING](CONTRIBUTING.md)（贡献与案例编写规范）、[STATUS](STATUS.md)（当前快照）、[ROADMAP](ROADMAP.md)（路线图）、[CHANGELOG](CHANGELOG.md)（版本变更）。

## 本地预览与构建

```bash
npm install -g mystmd
BASE_URL=/quanttide-gallery-of-business-entity myst start           # 本地预览
BASE_URL=/quanttide-gallery-of-business-entity myst build --html    # 构建到 _build/html
```

`BASE_URL` 不能省。省掉时产物里的资源路径与站内链接都是根路径（`/build/_assets/…`、`/qtdata`），本地能看，发到 GitHub Pages 项目站会全部 404。

## 发布

推 `main` 触发 `.github/workflows/deploy.yml`：安装 mystmd → `myst build --html` → 部署到 GitHub Pages。
