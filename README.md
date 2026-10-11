# 心愿之间 · WishTwo

一个以互相送礼为核心的双人心愿网站原型。支持个人心愿、分享设置、预算筛选、特别想要、存钱记录及撤销、完成/恢复/归档，以及共同计划。

## 本地开发

需要 Node.js 20.19+ 或 22.12+。

```sh
npm ci --cache /workspace/.npm-cache
npm run dev
```

```sh
npm run build
npm run preview
```

## 当前范围

这是可交互的前端原型，使用 React + Vite。数据保存在当前浏览器的 localStorage；首页对方的心愿是演示数据。没有真实账号、邀请绑定、多人权限和跨设备同步。页面中的私密及分享状态只演示产品交互，不构成服务端访问控制。清除浏览器数据会清除本地记录。插画为本地 SVG，字体来自 Google Fonts；字体不可用时使用系统字体。

下一阶段需接入账号及数据库，并在服务端验证空间成员和心愿访问权限，再实现邀请、解除绑定和共同清单历史保留。

## 发布到 GitHub Pages

仓库 Settings → Pages → Build and deployment → Source 选择 GitHub Actions。推送到 main 后，`.github/workflows/pages.yml` 会构建并发布 `dist`。也可以在 Actions 中手动运行 Deploy website to GitHub Pages。部署成功后，Pages 设置页会显示正式网址。

公开部署的是演示网站，不会同步不同用户的心愿；本地记录仅在各自浏览器中保存。

## Superdesign 设计技能

完整技能已安装在 `.agents/skills/superdesign/`，适用于支持项目级 `.agents/skills` 的 AI 编程助手（如 Codex）。这是给 AI 助手使用的设计流程，不是网站运行依赖；`npm run dev` 不会自动运行它。

在项目目录启动你的 AI 编程助手后，可以要求：

> 使用 superdesign 技能优化心愿之间的首页，保留互相送礼、个人心愿和共同清单的功能。

Superdesign 在线画布需另外登录。在终端可使用按需 CLI，无需全局安装：

```sh
npx --yes @superdesign/cli@latest
npx --yes @superdesign/cli@latest login
```

登录与生成由设计任务按技能流程执行；生成可能消耗 Superdesign 账户额度。首次设计前需分析现有代码，生成 `.superdesign/init/` 上下文。当前只安装技能，尚未登录或生成设计稿。

Windows 用户：从 GitHub 下载最新 ZIP 并解压后，技能也在项目的 `.agents/skills/superdesign/` 内。已经下载的旧 ZIP 不会自动更新。请保留本地修改，再下载新版或仅复制新版 `.agents` 文件夹到现有项目。
