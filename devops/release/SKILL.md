---
name: release
description: 版本发布技能，遵循语义化版本规范，用于创建 Git 标签、更新 CHANGELOG 并发布 GitHub Release。当需要发布新版本、打标签、更新发布说明时使用。
---

# 版本发布技能

用于 quanttide-gallery-of-business-entity 仓库的版本发布流程。

## 发布前检查

1. 确认所有变更已提交:
   ```bash
   git status
   git log <last-version>..HEAD --oneline
   ```

2. 确认发布就绪:
   - [ ] 所有变更已提交
   - [ ] 无未跟踪文件
   - [ ] CHANGELOG.md 存在

## 更新 CHANGELOG

1. 编辑 `CHANGELOG.md`，在首个版本标题前插入新版本:
   ```markdown
   ## [<version>] - <YYYY-MM-DD>

   ### Added
   - 新增内容

   ### Changed
   - 修改内容

   ### Fixed
   - 修复内容

   ### Removed
   - 移除内容
   ```

2. 分类标签说明:
   - **Added**: 新增功能或文件
   - **Changed**: 已有内容的修改
   - **Fixed**: 问题修复
   - **Removed**: 删除的内容

3. 提交并推送:
   ```bash
   git add CHANGELOG.md
   git commit -m "chore: update CHANGELOG for <version>"
   git push origin main
   ```

## 创建 Git 标签

1. 创建附注标签:
   ```bash
   git tag -a <version> -m "Release version <version>"
   ```

2. 推送标签到远程:
   ```bash
   git push origin <version>
   ```

## 创建 GitHub Release

使用 GitHub CLI 创建 Release:

```bash
gh release create <version> \
  --title "<version>" \
  --generate-notes
```

Release URL: `https://github.com/quanttide/quanttide-gallery-of-business-entity/releases/tag/<version>`

## 更新主仓库引用

在主仓库中更新子模块引用:

```bash
cd /home/iguo/repos/quanttide-tech
git add docs/gallery
git commit -m "chore: 同步 docs/gallery 子模块，发布 <version>"
git push
```

## 发布后确认

- [ ] CHANGELOG.md 已更新并提交
- [ ] Git 标签已创建并推送
- [ ] GitHub Release 已创建
- [ ] 主仓库子模块引用已更新并推送

## 版本号规则

遵循语义化版本: `主版本.次版本.修订号`

- **主版本**: 不兼容的重大修改
- **次版本**: 向后兼容的功能新增
- **修订号**: 向后兼容的问题修复

当前为早期阶段，版本号格式: `0.0.x`
