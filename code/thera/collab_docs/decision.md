# 实时协作云文档技术决策

## 背景

飞书文档格式封闭且性能较差，需要自建局域网实时协同文档系统。

## 方案对比

### 核心技术选型

| 方案 | 优点 | 缺点 |
|------|------|------|
| **CRDT + Yjs** | 自动冲突解决、离线支持、P2P能力、成熟生态 | 学习曲线 |
| OT + ShareDB | Google Docs 采用 | 需要中心服务器、维护不活跃 |
| 自研 | 完全可控 | 工作量大、难以保证正确性 |

### 推荐技术栈

| 层级 | 技术选型 | 理由 |
|------|----------|------|
| **CRDT** | Yjs | 2.5M 周下载量、MIT 协议、网络无关、成熟稳定 |
| **后端** | Hocuspocus | Yjs 官方推荐、SQLite/PostgreSQL 持久化、Tiptap 团队维护 |
| **富文本编辑器** | Tiptap | Yjs 官方绑定、React/Vue 支持、扩展丰富 |
| **通信** | WebSocket | 实时同步、低延迟 |
| **可选 P2P** | y-webrtc | 无需服务器、点对点连接 |

## 决策

采用 **Yjs + Hocuspocus + Tiptap** 技术栈。

### 架构设计

1. **单机模式**：一台机器运行 Hocuspocus WebSocket 服务器，其他机器通过局域网 IP 连接
2. **P2P 模式**（可选）：使用 y-webrtc，完全去中心化，无需服务器

### 部署方式

- 本地 SQLite 存储
- Docker 一键部署
- 局域网 IP 访问

## 待验证问题

- [ ] 大文档性能
- [ ] 离线编辑与同步
- [ ] 多端光标冲突

## 参考资源

- [Yjs 官方文档](https://docs.yjs.dev)
- [Hocuspocus](https://hocuspocus.dev)
- [Tiptap](https://tiptap.dev)
