# 贡献指南

## 贡献方式

报告问题通过 GitHub Issues，提交修改通过 Pull Request。

## 提交流程

本仓库是 `quanttide-tech` 的子模块，改完要逐层回到父仓库：

1. 子模块内提交推送：`git commit -m "docs: …"`、`git push`
2. 更新父仓库指针：在 `quanttide-tech` 里 `git add docs/gallery && git commit -m "chore: update gallery submodule"`、`git push`
3. 若父仓库也在根仓库的子模块里，再更新 `quanttide` 的 `default/quanttide-tech` 指针

提交信息用 Conventional Commits（`docs:` / `fix:` / `chore:`）。

## 案例编写规范

案例是按业务线组织的：一个业务线一个目录，目录内一个 `index.md` 作入口，具体案例作为同目录下的文件挂在它后面。

一个案例页回答三件事：这条业务是什么、它分哪几类、每一类里我们实际怎么做（给真实做法与数字）。分类要跟业务的**真实交付方式**走，不要套统一模板——量潮数据按加工阶段分（采集／清洗／大模型挖掘）、量潮课堂按招生方式分（校企合作／社会招生）、量潮云按产品形态分（SaaS／PaaS）、量潮咨询按客户类型分（创业／创新）。

口径上守三条：价格不写、客户不点名、未完成的产品如实说明状态。宁少而准：案例不是文章，是口径——谁读都不会误解我们在卖什么。

取材以创始人给的原始说法为准。各内容仓库里同一条业务有多个版本（宣传册偏客户视角、手册偏操作、随笔偏主张），写案例时取宣传册与教程的对外口径，把内部分析语汇压回去。

## 编写规范

遵循量潮科技文档格式标准：删除不必要的格式元素，优先用段落和标题；能用列表就不表格，能用文字就不列表；同一概念全程使用相同名称。

格式标准详见：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/docs/format.md

## 文档格式优化

文档完成后、提交前，对照格式规范检查一遍：加粗是否过度（列表项内、连续多个、标记所有术语）；列表是否滥用（简单对应关系、可段落化的内容）；标题层级是否过深（四级及以上）；引号是否用中文引号。改完跑一次 `BASE_URL=/quanttide-gallery-of-business-entity myst build --html`，确认构建通过、站内链接没断。
