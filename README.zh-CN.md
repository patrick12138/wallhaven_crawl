# wallhaven_crawl

[English](./README.md) | [简体中文](./README.zh-CN.md)

一个轻量的 Node.js 爬虫脚本，用于从 Wallhaven 的搜索/列表页面批量下载壁纸。

## 功能特性

- 从 Wallhaven 列表/搜索页面解析壁纸详情链接。
- 组装 `.jpg` 与 `.png` 的直链地址。
- 下载文件到本地目录。
- 当 `.jpg` 不可用时自动回退下载 `.png`。
- 同时支持单页下载和多页批量下载流程。

## 环境要求

- Node.js 14+（推荐）
- npm

## 安装

```bash
npm install
```

## 使用方式

当前脚本逻辑写在 `index.js`，直接运行：

```bash
node index.js
```

默认会执行文件底部的 `downAllImg()`。

## 配置说明

当前项目是脚本驱动（暂未提供命令行参数）。  
请按需求编辑 `index.js` 中以下位置：

- `getImgUrl()` 里的目标页面 URL
- `for` 循环中的页数范围
- 下载输出目录（例如 `./wallhaven_plants/`）

## 注意事项

- 运行前请确认目标下载目录已存在。
- 建议控制请求频率，避免对源站造成过大压力。
- 项目仅用于学习和个人用途，请遵守 Wallhaven 的使用条款与版权要求。
