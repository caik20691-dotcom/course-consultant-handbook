# GitHub Pages 手册首页设计

## 目标

访问 `https://caik20691-dotcom.github.io/course-consultant-handbook/` 时，直接展示《课程顾问岗位手册》正文，不需要用户再次点击或等待跳转。

## 方案

- 在仓库根目录新增 `index.html`。
- `index.html` 与现有 `课程顾问岗位手册.html` 使用相同的完整页面内容。
- 保留原始中文文件名页面以及仓库中的其他文件，不改变现有链接。
- GitHub Pages 继续使用 `main` 分支根目录发布，不修改现有 Pages 配置。

## 数据与交互

页面是静态 HTML，不新增后端、表单、账号或外部数据传输。浏览器访问根地址时由 GitHub Pages 直接返回 `index.html`。

## 异常处理

- 若 Pages 构建失败，检查 GitHub Pages 构建状态和部署日志。
- 若根地址仍为 404，确认 `index.html` 已推送到 `main` 分支根目录，并等待 Pages 完成重新构建。

## 验收标准

- Pages 构建状态为 `built`。
- 根地址返回成功页面，而不是 404。
- 页面标题和正文与《课程顾问岗位手册》一致。
- 原有 `课程顾问岗位手册.html` 链接仍可访问。
