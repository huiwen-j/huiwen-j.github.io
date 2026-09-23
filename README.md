# Huiwen Jia's personal website

使用 AcademicPages / Minimal Mistakes 构建的 Jekyll 学术主页。

## 日常维护

| 内容 | 文件 |
|---|---|
| 首页、教育经历、研究方向 | `_pages/about.md` |
| Preprints、期刊和会议论文 | `_pages/publications.md` |
| 教学和审稿记录 | `_pages/teaching_services.md` |
| 顶部导航 | `_data/navigation.yml` |
| 姓名、联系方式、头像设置 | `_config.yml` |
| 当前头像 | `images/huiwenjia_photo.png` |
| 备用内容模板 | `templates/README.md` |

`_includes/`、`_layouts/`、`_sass/` 和 `assets/` 包含当前网站使用的主题、
样式、脚本和字体。日常添加论文或审稿记录通常不需要修改这些目录。

模板示例已整理到 `templates/`，该目录不会发布到网站。未使用的 collection
目前设为 `output: false`；启用方法见模板说明。`LICENSE` 保留主题许可。

## 本地预览

在安装 Ruby、Bundler 和所需依赖后，从仓库目录运行：

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

打开 `http://127.0.0.1:4000/`。修改 `_config.yml` 后需要重新启动预览服务。
生成的 `_site/`、`Gemfile.lock` 和 `node_modules/` 不提交。

只有修改主题 JavaScript 时，才需要运行 `npm install` 和 `npm run build:js`，
用源文件重新生成 `assets/js/main.min.js`。

## 分支与发布约定

- `master` 是正式网站分支。用户只说 “push” 时，仅推送 `master`。
- `codex/outdoor-trails-map` 是离线户外地图草稿，独立保存。
- 只有明确要求 “push map” 才推送地图分支；只有明确要求 “merge map” 才合并地图。
- 本地修改和预览不代表已经发布。

基于 [AcademicPages](https://github.com/academicpages/academicpages.github.io)
和 [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)，原许可见 `LICENSE`。
