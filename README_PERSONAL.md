# 个人主页维护指南

## 项目概览

基于 [academicpages](https://github.com/academicpages/academicpages.github.io) 模板的 Jekyll 静态个人学术主页。

- **网址**：https://ronghuiguo.github.io
- **上游**：https://github.com/academicpages/academicpages.github.io
- **主题**：Minimal Mistakes → academicpages
- **托管**：GitHub Pages（推送 `main` 即自动部署）

---

## 本地预览

### 首次安装

```bash
# 安装 Ruby（只需一次）
sudo apt update && sudo apt install -y ruby-dev ruby-bundler nodejs

# 配置 bundler 安装到用户目录
bundle config set --global path '~/.gem'

# 安装依赖
bundle install
```

### 启动预览

```bash
cd ~/Code/RonghuiGuo.github.io
bundle exec jekyll serve
# → 访问 http://localhost:4000
```

修改文件后终端会自动检测并重建，刷新浏览器即可看到效果。

按 `Ctrl+C` 停止服务。

### 故障排查

| 问题 | 解决 |
|------|------|
| `PermissionError` | 运行 `bundle config set --global path '~/.gem'` |
| 端口被占用 | `bundle exec jekyll serve --port 4001` |
| 依赖版本冲突 | 删除 `Gemfile.lock` 后重新 `bundle install` |

---

## 主题定制

在 `_config.yml` 中修改：

```yaml
site_theme: "default"  # 可选：default / air / sunrise / mint / dirt / contrast
```

所有主题自动支持暗色模式（跟随系统设置）。修改后需重启 `bundle exec jekyll serve` 生效。

---

## 需要修改的文件地图

### 核心配置

| 文件 | 修改内容 | 备注 |
|------|----------|------|
| `_config.yml` | 站点标题、作者信息、社交链接、邮箱、ORCID、主题 | 大部分已填，Google Scholar 等链接待完善 |
| `_data/navigation.yml` | 顶部导航菜单 | 已配置，按需增删 |

### 页面内容

| 文件 | 修改内容 | 状态 |
|------|----------|------|
| `_pages/about.md` | 首页个人介绍 | ✅ 已填写 |
| `_pages/cv.md` | 个人简历 | ✅ 教育 + 论文 |

### 学术内容

| 目录 | 用途 | 状态 |
|------|------|------|
| `_publications/` | 论文，每个 `.md` 一篇 | ✅ 5 篇真实论文 |
| `_talks/` | 报告/演讲 | ⚠️ 模板占位，可删除或替换 |
| `_teaching/` | 教学经历 | ⚠️ 模板占位 |
| `_posts/` | 博客文章 | ⚠️ 模板占位 |
| `_portfolio/` | 作品集 | ⚠️ 模板占位 |

### 生成工具

| 文件 | 用途 |
|------|------|
| `markdown_generator/` | 从 TSV/CSV 批量生成 publications 和 talks 的 markdown |
| `talkmap.py` / `talkmap.ipynb` | 根据 _talks 生成演讲地点地图 |

### 模板文件（不应手动修改）

以下目录属于上游模板，修改会在同步时被覆盖：

- `_includes/` — HTML 组件
- `_layouts/` — 页面布局
- `_sass/` — 样式文件
- `assets/` — JS/CSS/字体

---

## 同步上游模板

上游仓库：https://github.com/academicpages/academicpages.github.io

⚠️ **由于历史已被压缩，不要用 `git merge`，使用手动同步模式：**

```bash
# 1. 拉取上游
git fetch upstream

# 2. 只同步模板文件目录（不覆盖个人文件）
git checkout upstream/master -- \
  _includes/ \
  _layouts/ \
  _sass/ \
  assets/

# 3. 如 Gemfile 或 package.json 有更新也可同步
git checkout upstream/master -- Gemfile package.json

# 4. 提交并推送
git add -A
git commit -m "chore: sync upstream template files"
git push origin main
```

这样 `_includes/`、`_layouts/`、`_sass/`、`assets/` 等模板目录会更新到最新版本，而 `_config.yml`、`_pages/`、`_publications/`、`images/` 等个人文件不受影响。

### 撤销同步

```bash
git reset --hard HEAD~1     # 撤销上次提交
git reset --hard origin/main # 回退到远程版本
```

---

## Git 操作备忘

### 提交并推送

```bash
git add -A
git commit -m "type: description"
git push origin main
```

如果因历史压缩需要强制推送：

```bash
git push -f origin main
```

### 压缩历史（清理敏感信息后使用）

```bash
git checkout --orphan clean-main
git add -A
git commit -m "Personal academic homepage"
git branch -D main
git branch -m clean-main main
git push -f origin main
```

---

## 常用操作速查

### 添加新论文

在 `_publications/` 下创建 markdown 文件：

```yaml
---
title: "论文标题"
collection: publications
category: conferences   # 或 manuscripts（期刊）
permalink: /publication/年份-简称
excerpt: '一句话摘要'
date: 2025-01-01
venue: '会议/期刊全称'
paperurl: 'https://doi.org/xxx'
citation: '作者. (年份). "标题." <i>期刊/会议</i>.'
---
摘要内容...
```

### 切换主题

编辑 `_config.yml` 中 `site_theme` 字段，修改后重启预览。

### 隐藏某篇论文

在论文的 YAML 头中加入 `published: false`。

---

## 待办清单

- [ ] 删除 `_talks/` 中的模板占位报告
- [ ] 删除 `_teaching/` 中的模板占位教学
- [ ] 删除 `_posts/` 中的模板占位博客
- [ ] 删除 `_portfolio/` 中的模板占位作品
- [ ] 完善 `_config.yml` 中的 Google Scholar 链接
- [ ] 考虑启用评论系统（`comments.provider`）
- [ ] 考虑启用 Google Analytics（`analytics.provider`）
