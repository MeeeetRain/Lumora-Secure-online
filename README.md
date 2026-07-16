# Lumora Secure 内测版

Lumora 是面向 Apple Silicon Mac 的实时 SDR→HDR 播放与采集工具。本仓库仅用于分发加密内测安装包，不包含源代码、模型或安全实现细节。

## 系统要求

- Apple Silicon Mac（M 系列芯片）
- macOS 13.0 或更高版本
- 首次激活时需要连接互联网
- 使用采集卡或上屏卡时，需要先安装厂商驱动

## 安装与首次使用

1. 从 [Releases](https://github.com/MeeeetRain/Lumora-Secure-online/releases) 下载最新版 `Lumora-Secure-online.dmg`。
2. 打开 DMG，将 `Lumora-Secure.app` 拖入“应用程序”文件夹。
3. 首次启动后填写接收授权邮件的邮箱，点击发送验证码/授权码。
4. 收到邮件后，将授权码或整段邮件内容粘贴到授权框；App 会自动识别其中以 `LMRA-` 开头的授权码。
5. 点击“验证授权码并进入”。授权码首次验证后会与当前 Mac 绑定。

## 授权说明

- 一个授权码同一时间仅绑定一台 Mac；换机前需要由管理员解绑。
- App 启动及运行期间会定期与授权服务器核验。
- 每次在线核验成功后，可获得最长 48 小时离线使用时间。
- 请勿转发授权邮件或授权码。

## macOS 安全提示

当前内测包尚未完成 Apple Developer ID 公证。首次打开若被 macOS 阻止，请在 Finder 中右键 App 选择“打开”；仍被阻止时，前往“系统设置 → 隐私与安全性”，确认来源后选择“仍要打开”。仅应使用本仓库 Release 中提供的安装包，并核对随附的 SHA-256 文件。

校验命令：

```bash
shasum -a 256 -c Lumora-Secure-online.dmg.sha256
```

## 基本操作

- 本地播放：在首页选择视频文件，或将视频拖入窗口。
- 采集模式：连接并安装好采集设备后，在 App 中进入采集输入。
- SDR/HDR 与增益预览：通过播放器界面对应的显示模式切换。
- DeckLink/SDI 输出：连接设备并安装 Blackmagic Desktop Video 后，在输出选项中选择相应设备。

本版本为内部测试用途。如遇到授权、设备绑定、视频兼容或采集输出问题，请记录 macOS 版本、Mac 型号、设备型号和复现步骤后反馈。
