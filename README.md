# Class Feedback Assistant

本仓库只提供已验证的 Windows 发布包下载，不包含应用源码。

## 下载

最新版下载：

```text
https://github.com/noonwendy/class-feedback-assistant-download/releases/latest/download/class-feedback-assistant-windows.zip
```

当前公开版本：`v0.1.6`

SHA256：

```text
175D07E042D375034B24FC79281A79BC862B841A6C0EF0FBEAEDD856A4A7CECB
```

## 启动

1. 下载 `class-feedback-assistant-windows.zip`。
2. 完整解压，不要直接在压缩包里运行。
3. 双击 `start-assistant.bat`。
4. 浏览器打开后进入“设置中心”完成配置和测试。

如果双击没有反应，在解压目录打开 PowerShell：

```powershell
.\start-assistant.ps1
```

## 更新

应用内“设置中心”可以检查公开版本。需要更新时，先关闭当前程序，再在解压目录运行：

```powershell
.\update-assistant.ps1
```

只检查版本：

```powershell
.\update-assistant.ps1 -CheckOnly
```

## 卸载

删除程序文件但保留本地数据：

```powershell
.\uninstall-assistant.ps1
```

同时删除本地运行数据：

```powershell
.\uninstall-assistant.ps1 -RemoveData
```

## 安全说明

这是一个本地 Windows 桌面自动化工具，运行时会控制本机桌面消息客户端完成经过确认的发送任务。请只从本仓库 Release 下载，并在需要时比对 SHA256。

发布包已在 GitHub Actions 中完成自动测试、启动 smoke test 和 Microsoft Defender 扫描。
