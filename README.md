# 董庆黎的个人主页（GitHub Pages 版）

线上地址：<https://Qingli-DONG.github.io>

只包含：**个人主页 + 两篇 MHE 学习笔记**（第 3 章、第 4 章）。

## 文件说明

| 文件/文件夹 | 作用 |
|---|---|
| `index.html` | 主页（关于 / 研究 / 项目 / 笔记 / 技能 / 联系） |
| `style.css` | 主页样式（克莱因蓝 · 编辑排版风，零外部依赖） |
| `notes/MHE_第3章_笔记.html` | 第 3 章《回归的基本原理》完整笔记（含公式渲染） |
| `notes/MHE_第4章_笔记.html` | 第 4 章《工具变量回归》完整笔记（含公式渲染） |
| `mathjax-es5/` | 公式渲染引擎（本地优先，加载失败自动切换 CDN 兜底） |
| `.gitignore` | 排除本地留档的旧版备份（`_备份_*/`） |

## 一、本地预览

直接双击 `index.html` 用浏览器打开即可预览；两篇笔记在 `notes/` 里，可单独双击打开。

## 二、部署（推送即上线）

仓库已建好：<https://github.com/Qingli-DONG/Qingli-DONG.github.io>（Public）。
本文件夹已初始化为该仓库的本地 git 仓库，**推送即上线**，`git push` 后 1—2 分钟自动更新。

日常更新：

```bash
cd "D:\stata18\ado\personal\董庆黎的实证_OFDI_海关\github_homepage"
git add .
git commit -m "更新说明"
git push
```

换电脑时恢复：

```bash
git clone https://github.com/Qingli-DONG/Qingli-DONG.github.io.git
```

## 三、以后如何更新笔记

笔记源文件在 `C:\Users\董庆黎\Desktop\个人\学习\科研\计量学习\MHE\notes\`。

更新步骤：

1. 把新导出的笔记 HTML 复制到本文件夹的 `notes/` 下
2. 文件名保持 `MHE_第3章_笔记.html`、`MHE_第4章_笔记.html` 不变（直接覆盖）
3. `git add . && git commit -m "更新笔记" && git push`，主页入口无需任何改动

## 四、常见问题

- **公式不显示**：确认 `mathjax-es5` 文件夹已推送到仓库根目录；笔记里做了 CDN 兜底，本地文件缺失时自动从 CDN 加载，多等几秒即可
- **改了文件网站没变**：GitHub Pages 有 1—2 分钟部署延迟，另可 Ctrl+F5 强制刷新清除缓存
- **主页样式丢失**：确认 `style.css` 和 `index.html` 都在仓库**根目录**（不能放进子文件夹）
- **想改回旧版**：`git log --oneline` 找到改版前的提交，`git checkout <commit> -- index.html style.css`
