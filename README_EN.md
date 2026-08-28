<div align="center">

# VpnLine 🔒

**Private VPN management, Claude Code automation skill**

Manage your private VPN infrastructure with Claude Code automation.

[![GitHub Stars](https://img.shields.io/github/stars/iTrimut/VpnLine?style=social)](https://github.com/iTrimut/VpnLine/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/iTrimut/VpnLine)](https://github.com/iTrimut/VpnLine/issues)
[![GitHub Forks](https://img.shields.io/github/forks/iTrimut/VpnLine?style=social)](https://github.com/iTrimut/VpnLine/network/members)
[![License](https://img.shields.io/github/license/iTrimut/VpnLine)](LICENSE)

[English](README_EN.md) | [中文](README.md)

</div>

---

## About

VpnLine is a **Claude Code Skill** for managing personal VPN infrastructure. When you mention VPN-related operations in Claude Code, this skill is automatically loaded and executed.

Supports macOS, iPhone, and Android with dual-line redundancy architecture and automatic local proxy switching.

## Features 🎯

- **Claude Code Integration** — mentioning VPN auto-loads the skill
- **Dual-line Redundancy** — Shadowsocks primary + IKEv2 fallback
- **Multi-platform** — macOS menu bar toggle / iPhone Shadowrocket / Android SS client
- **Auto Proxy Switching** — proxy env vars auto-set/clear on VPN connect/disconnect
- **One-click Ops** — service status check, restart, firewall management
- **New Device Setup** — auto-generate client config files

## Quick Start 🚀

### macOS (Recommended)

Desktop `US VPN.app` — click to connect/disconnect.

Or terminal:
```bash
/opt/homebrew/opt/shadowsocks-libev/bin/ss-local -c /opt/homebrew/etc/shadowsocks-libev.json
```

### iPhone / iPad

1. Download **Shadowrocket** (paid) or **Outline** (free) from App Store
2. Scan `ss://` QR code or enter config manually
3. Connect

### Android

1. Download [Shadowsocks for Android](https://github.com/shadowsocks/shadowsocks-android)
2. Scan QR code or configure manually
3. Connect

## Installation 📥

### ① Clone to Claude Code

```bash
cd your-project
git clone https://github.com/iTrimut/VpnLine.git .claude/skills/upup-vpn
```

### ② Verify

Type VPN-related keywords in Claude Code (e.g. "connect VPN") to confirm the skill loads.

### ③ Configure Credentials

`references/credentials.md` is a committed **non-sensitive template** (server IP, ports, protocol).
Real passwords / keys / tokens live locally only (`TOOLS.md` / `memory/`) — **never commit them**.

## FAQ 🤔

❓ Q: macOS 26.5 mobileconfig doesn't create VPN service?
A: Use Shadowsocks client instead, or check System Preferences → VPN.

❓ Q: AppleScript .app shows "unverified developer"?
A: Right-click → Open, or System Settings → Privacy & Security → Open Anyway.

❓ Q: ss-local disconnects?
A: Restart ss-local or use the reconnect script.

## Feedback 📢

Submit [Issues](https://github.com/iTrimut/VpnLine/issues) and [Pull Requests](https://github.com/iTrimut/VpnLine/pulls).

## License 📝

[MIT License](LICENSE)

---

<div align="center">

**Private VPN, Secure Internet**

</div>
