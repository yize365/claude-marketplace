# Disk Cleaner for Claude Code

Windows C 盘空间分析与动态清理工具。零配置，全自动发现可清理内容。

## 特性

- **全动态扫描**：无需预知应用名，自动发现任何机器上的缓存/日志/更新器
- **三级清理**：🟢安全 / 🟡谨慎 / 🟠深度，按需选择
- **安全优先**：不触碰用户数据、聊天记录、系统文件
- **可预览**：`--dry-run` 模式先看再删

## 安装

```bash
claude plugin marketplace add https://github.com/yize365/claude-marketplace
claude plugin install disk-cleaner@yize365-toolbox
```

## 使用

直接对 Claude 说：
- 「C盘满了帮我清理」
- 「分析C盘空间占用」
- 「释放磁盘空间」

或手动运行脚本：
```powershell
# 分析
powershell -File scripts/analyze_disk.ps1
powershell -File scripts/analyze_user.ps1

# 清理（可选 --dry-run 预览）
powershell -File scripts/cleanup_green.ps1
powershell -File scripts/cleanup_yellow.ps1
powershell -File scripts/cleanup_deep.ps1
```
