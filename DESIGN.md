# 项目介绍与设计

> 此文档针对本项目功能进行简短的介绍与设计

## 功能

- 端到端加密通信
- 跨节点交换数据
- 动态端口转发
- 支持部署在 HTTP/HTTPS 后端
- 支持 NAT

## 设计

### 协议选型

- `TCP - TLS 1.3(rfc8446)` : 基于 `TLS 1.3` 完成端到端加密。
- `UDP - QUIC(rfc9000) - TLS 1.3(rfc8446)`:  基于 `QUIC-TLS` 完成端到端加密。
- `HTTP(s) - WebSocket(rfc6455) - TLS 1.3(rfc8446)`: 基于 `ws - tls1.3` 完成端到端加密。
- `TCP/UDP - plain` : 无传输层加密，仅适用于可信网络。

### 扩展

- `mTLS`
- `ESNI`
- `X.509v3`
