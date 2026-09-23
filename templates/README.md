# 备用内容模板

每类只保留一个参考示例。`_config.yml` 已排除整个 `templates/` 目录，
这里的 Markdown、图片和 PDF 不会生成网页，也不会进入 sitemap。

这些是格式示例，里面的姓名、日期、学校和论文信息都是占位内容。
使用前请替换正文、标题、日期、链接、`permalink` 和重定向地址。

| 模板 | 将来启用时放到哪里 |
|---|---|
| `publication.md` | `_publications/YYYY-MM-DD-paper-name.md` |
| `blog-post.md` | `_posts/YYYY-MM-DD-post-name.md` |
| `talk.md` | `_talks/YYYY-MM-DD-talk-name.md` |
| `teaching.md` | `_teaching/YYYY-term-course.md` |
| `portfolio.md` | `_portfolio/project-name.md` |
| `cv.md` | `_pages/cv.md` |
| `page.md` | `_pages/new-page.md` |
| `markup.md` | Markdown 排版语法参考；通常只复制需要的片段 |
| `files/paper1.pdf` | 一份示例论文 PDF；实际使用时上传真实 PDF 到 `files/` |
| `files/slides1.pdf` | 一份示例幻灯片 PDF；实际使用时上传真实 PDF 到 `files/` |
| `images/500x300.png` | 一份占位图；使用作品模板时复制或替换到 `images/` |

## 当前网站内容

真实论文列表直接维护在 `_pages/publications.md`，教学和审稿记录维护在
`_pages/teaching_services.md`；日常更新这两个页面不需要启用 collection。

## 启用新的栏目

1. 从上表复制所需模板到对应目录，并替换占位内容。
2. 如果启用 publications、talks、teaching 或 portfolio 的独立条目页面，
   将 `_config.yml` 中对应 collection 的 `output` 改为 `true`。
3. 如需栏目索引，在 `_pages/` 新建一个 `layout: archive` 的页面，遍历
   对应的 `site.publications`、`site.talks`、`site.teaching` 或 `site.portfolio`。
   可使用保留的 `_includes/archive-single.html` 渲染每个条目。
4. 需要导航入口时，编辑 `_data/navigation.yml`。
5. 修改 `_config.yml` 后重启本地预览，确认只发布准备好的内容。

博客按 `_posts/` 的日期文件名自动生成；`future: false` 会隐藏未来日期的文章。
普通页面与博客不需要修改 collection 的 `output`。

模板来源：AcademicPages / Minimal Mistakes；许可保留在仓库根目录 `LICENSE`。
