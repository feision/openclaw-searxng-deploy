# 🔍 SearXNG 部署指南

> 私有 SearXNG 实例完整部署与 OpenClaw 集成教程

## 📖 这是什么？

本仓库提供从零开始部署私有 SearXNG 搜索引擎的完整指南，并教你如何将其集成到 OpenClaw AI 助手中。

**适合人群**：
- 注重隐私、不想被追踪的开发者
- 需要自建搜索后端的 AI 应用
- 有 Docker/VPS 环境的运维人员

## 🚀 快速开始

👉 阅读 [SEARXNG_DEPLOYMENT.md](SEARXNG_DEPLOYMENT.md) 开始部署。

主要步骤：
1. Docker Compose 一键部署
2. 修改 `settings.yml`（关键：`formats`, `bind_address`, `public_instance`）
3. 验证 JSON API
4. 创建 OpenClaw 工具 `~/.openclaw/tools/searxng.js`
5. 开始搜索！

## 📂 文件结构

```
searxng-deployment-guide/
├── README.md                 # 本文件
├── SEARXNG_DEPLOYMENT.md    # 完整教程（含故障排查）
└── .gitignore
```

## ⚡ 核心要点

- ✅ **Docker Compose** 推荐方式，5 分钟部署
- ✅ **三个关键配置**：`formats: [html, json]`、`bind_address: "0.0.0.0"`、`public_instance: true`
- ✅ **OpenClaw 集成**：通过工具（`~/.openclaw/tools/`）而非配置文件
- ✅ **完整验证流程**：`curl` 命令确保 JSON API 可用
- ✅ **Zeabur 特殊说明**：附录提供云平台适配

## 📝 许可

本教程基于 [SearXNG 官方文档](https://docs.searxng.org/) 编写，遵循原项目许可证（AGPL-3.0）。

---

**保持简洁，快速部署。** 🎯
