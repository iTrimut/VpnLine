# upup-vpn Credentials & Server Info

> ⚠️ **敏感信息不入库**：本文件是**模板**，仅包含非敏感的基础设施信息（IP、端口、协议等），
> 供技能加载时读取。真实密码 / 密钥 / token 统一存放在本机 `~/.vpnline/upup.secrets.json`
> （详见 `~/.vpnline/README.md`），绝不提交到仓库。

## Server

- IP: 164.92.75.99 (San Francisco SFO3)
- Droplet ID: 573298872
- OS: Ubuntu 22.04 LTS
- Rebuilt: 2026-05-26（旧服务器 144.126.210.202 因网络问题已删除）
- SSH: Key-based auth（本机 `~/.ssh/id_ed25519`）

## Services

- Shadowsocks: Port 8388, chacha20-ietf-poly1305（密码见本地记录）
- IPsec/L2TP + IKEv2

## 客户端配置文件（位于服务器）

- `/root/vpnclient.mobileconfig` — iOS/macOS
- `/root/vpnclient.sswan` — Android StrongSwan
- `/root/vpnclient.p12` — 证书文件
- 重新导出: `ssh root@<IP> "sudo ikev2.sh --exportclient <name>"`

## 真实凭据（不入库）

- 位置: `~/.vpnline/upup.secrets.json`（本机，Mac / Windows 通用）
- 内容: Shadowsocks 密码、DigitalOcean API token 等
- 若缺失: 按 `~/.vpnline/README.md` 从 Mac 的 `/opt/homebrew/etc/shadowsocks-libev.json` 与 `TOOLS.md`/`memory/` 填充
- 规则: 任何 VPN 任务开始时都要读取该文件；禁止打印 / 提交 secret 值

*Actual passwords and tokens are stored locally, not in this repository.*
