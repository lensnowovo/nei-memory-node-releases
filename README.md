# N.E.I. Memory Node · Windows Preview

这里是 N.E.I. Memory Node 的官方 Windows 安装包仓库。

Memory Node 让 Codex、WorkBuddy 等 Agent 在不同任务间读取和沉淀经过确认的长期投资记忆。记忆数据库保存在用户选择的本机固定磁盘目录中，不上传到本仓库或 `nei-pevc.com`。

## 下载

前往 [Releases](https://github.com/lensnowovo/nei-memory-node-releases/releases/latest) 下载最新版：

- 普通用户优先选择 `N.E.I. Memory Node_*_x64-setup.exe`；
- MSI 主要用于需要标准 Windows Installer 的环境；
- `SHA256SUMS.txt` 用于核对安装包；
- `release-manifest.json` 记录版本、来源提交、文件大小和实际签名状态。

## 当前版本是什么性质？

当前为 Windows Preview，适合受邀测试与个人试用，还不是面向机构批量部署的正式稳定版。

安装包暂未使用受公众信任的 Authenticode 证书签名。Windows 可能显示“未知发布者”或 SmartScreen 提示。请只从本仓库或 [nei-pevc.com](https://nei-pevc.com/memory) 下载，并在安装前核对 SHA-256。

## 第一次使用

1. 安装并打开 Memory Node；
2. 使用 N.E.I. 账号登录；
3. 选择本机记忆目录；
4. 让客户端自动识别并连接 Codex 或 WorkBuddy；
5. 按客户端提供的体验指令确认第一条记忆，再重新召回验证。

Memory Node 不需要一直显示在桌面。Agent 通过已配置的本地 MCP launcher 按需启动它。

## 核对 SHA-256

在安装包所在目录打开 PowerShell：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\N.E.I. Memory Node_0.1.4_x64-setup.exe'
```

结果应与同一 Release 中 `SHA256SUMS.txt` 的对应值完全一致。

## 隐私与安全边界

- 不要在 Issue 中上传数据库、记忆目录、项目材料、Token、许可证或日志原文；
- 网站只接收账号激活所需的最少设备授权元数据，不接收机构、基金、项目或记忆正文；
- 当前数据库为本机明文 SQLite，请使用 Windows 设备加密或 BitLocker，并保持可恢复备份；
- 当前不提供跨设备同步；复制数据库文件不等于安全的账号迁移。

安全问题请阅读 [SECURITY.md](SECURITY.md)。一般问题可以提交 [Issue](https://github.com/lensnowovo/nei-memory-node-releases/issues)。

## 关于源码

本仓库只用于分发官方安装包和公开发布说明，不包含 Memory Node 源码，也不授予源码许可。产品主页：[nei-pevc.com/memory](https://nei-pevc.com/memory)。
