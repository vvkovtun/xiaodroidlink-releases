# XiaoDroidLink — 用户指南

语言：[English](README.md) · [Українська](README.ua.md) · [中文](README.zh.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Polski](README.pl.md) · [Қазақша](README.kk.md) · [Azərbaycanca](README.az.md) · [Oʻzbekcha](README.uz.md) · [Тоҷикӣ](README.tg.md) · [ქართული](README.ka.md) · [Հայերեն](README.hy.md) · [Кыргызча](README.ky.md)

XiaoDroidLink 可以通过 CarLink 将 Android 手机连接到小米 YU7 车机屏幕。它可以在车机上显示仪表盘或手机屏幕，控制音乐，打开选定应用，把车机触摸操作传回手机，并通过屏幕投射显示 Google Maps。

这是一个独立项目，不是 Xiaomi、Samsung、ICCOA、Android Auto 或 Google 的官方产品。

## 功能

- 连接小米 YU7 CarLink。
- 输入车机屏幕上的 6 位验证码完成配对。
- 由小组件组成的主屏幕：最多三个屏幕、五种预设布局、23 个小组件（地图、下一个转弯、车速、测速摄像头、充电站、回家/公司路线、音乐、消息、联系人、日历、手机应用窗口等）。可在车机屏幕上排列、调整大小和设置：齿轮 → 小组件。
- 提供八种设计，每种都有地图、媒体和行程预览。底部的“屏幕 1/3 ›”按钮可切换三个实时屏幕，齿轮按钮可打开设计目录。
- 来电卡片，带“接听”和“拒接”按钮。
- 手机屏幕模式：在车机屏幕上显示手机应用。
- 通过 Android 无障碍服务把车机触摸操作传回手机。
- 媒体控制：播放/暂停、上一首、下一首。
- 通过手机屏幕投射在仪表盘中显示所选地图应用；默认使用 Google Maps。
- 当蓝牙音频不可用时，可通过 CarLink 传输音频。
- 可选择要显示在车机中的应用。
- 语音提醒：测速摄像头和空袭警报。
- 用你的语言使用车机助手：按方向盘按钮说出指令，手机用中文转告车辆。
- 支持 14 种语言：English、Українська、中文、Français、Español、Deutsch、Polski、Қазақша、Azərbaycanca、Oʻzbekcha、Тоҷикӣ、ქართული、Հայերեն、Кыргызча。

## 视频

英文演示（49 秒）：

[![XiaoDroidLink presentation in English](https://i.ytimg.com/vi/3C1UO75dUE4/hqdefault.jpg)](https://www.youtube.com/shorts/3C1UO75dUE4)

每项功能和小组件的详细说明（英文）：[All features](FEATURES.md) · [Home screen widgets](WIDGETS.md)。

## 从 Google Play 安装

XiaoDroidLink 已在 Google Play 上架。

1. 在手机上用 Google Play 打开 XiaoDroidLink：[https://play.google.com/store/apps/details?id=salon.lifestyle.xiaodroidlink](https://play.google.com/store/apps/details?id=salon.lifestyle.xiaodroidlink)
2. 点按“安装”。
3. 打开 XiaoDroidLink。

之后更新会通过 Google Play 自动推送。

如果你之前用 APK 文件安装过 XiaoDroidLink，请先卸载：APK 和 Google Play 版本签名不同，Google Play 无法覆盖安装。重新安装后，请再次输入车机屏幕上的代码。

## 适用的手机

- Android 13 或更新版本。
- 已在车上用 Samsung Galaxy S25 Ultra 测试。
- 视频编码器较弱的手机（许多联发科和紫光展锐机型，如 Infinix、Tecno、部分 Galaxy A）会向车机发送比例相同、稍小的画面。“无车预览”在这些手机上可用（已在 Infinix Hot 40 上验证）；车上尚未测试。如果画面没有铺满屏幕或没有显示，请发邮件至 xiaodroidlink@lifestyle.salon。

## 截图

在手机应用中可通过“无车预览”查看仪表盘。

| 车机屏幕预览 |
|---|
| ![XiaoDroidLink 中文车机仪表盘预览](images/xiaodroidlink-zh-car-preview.png) |

| 第 2 屏（共 3 屏）：媒体 | 第 3 屏（共 3 屏）：行程 |
|---|---|
| ![XiaoDroidLink media screen](images/xiaodroidlink-en-car-media.png) | ![XiaoDroidLink trip screen](images/xiaodroidlink-en-car-drive.png) |

| 设计目录 |
|---|
| ![XiaoDroidLink design catalog](images/xiaodroidlink-en-car-catalog.png) |

| 主屏幕 | 权限 |
|---|---|
| ![XiaoDroidLink main screen](images/xiaodroidlink-en-main.png) | ![XiaoDroidLink permissions screen](images/xiaodroidlink-en-permissions.png) |

| 设置 |
|---|
| ![XiaoDroidLink settings screen](images/xiaodroidlink-en-settings.png) |

## 首次设置

在 XiaoDroidLink 中打开 Permissions，并授予需要的权限：

- Bluetooth、location、microphone、notifications — 用于查找车辆、连接车机 Wi-Fi、音频和通知。
- Notification access — 用于音乐、Google Maps 提示和消息。
- Accessibility — 用于从车机屏幕控制手机应用。
- Modify system settings — 用于正确的屏幕方向。
- Unrestricted battery — 防止 Android 在后台中断连接。
- Screen casting — 用于 Google Maps 和手机屏幕模式。

## 连接车辆

1. 在小米 YU7 屏幕上打开 CarLink。
2. 在手机上打开 XiaoDroidLink。
3. 点击 Connect。
4. 如果 Android 请求屏幕投射权限，选择 Entire screen 并点击 Start。
5. 车机屏幕会显示 6 位验证码。
6. 在 XiaoDroidLink 中输入验证码。
7. 连接后选择 Dashboard 或 Phone screen 模式。
8. 行程结束后，在应用或通知中点击 Disconnect。

## 通过车辆蓝牙通话和语音

音乐通过 CarLink（Wi‑Fi）传到车上。通话、导航语音和 ChatGPT 走车辆蓝牙，需要单独连接。请在停车时操作。

1. 按上面的步骤连接车辆，等待车机屏幕出现画面。
2. 手机上会出现通知 `车辆蓝牙未连接`，点按它。
3. 应用会自动断开连接并打开蓝牙设置。在列表中选择你的车。
4. 不要再点其他东西。几秒钟后应用会自动重新连接，画面恢复。
5. 检查：通话或 ChatGPT 的声音应从车内扬声器播放。

需要了解：

- 不要在启动 CarLink 之前提前连接车辆蓝牙。CarLink 启动时车辆会断开这种连接。可靠的方式是通过通知操作。
- 如果蓝牙显示已连接，但通话仍从手机播放，请再次点按同一通知并重新选择车辆。
- 手机不会自动连接车辆蓝牙。每次行程开始时需要手动选择一次车辆。
- 选择车辆的时间为 90 秒。超时后应用会在没有蓝牙的情况下回到车机画面，通知会再次出现。
- 之后不要关闭车机屏幕上的 CarLink。只要它保持打开，蓝牙在断线和重新连接后仍会保持。如果关闭后重新打开，需要重复以上步骤。
- 蓝牙已连接时，音乐会在画面出现约 10 秒后才在车内播放。这是有意的延迟，避免车辆断开蓝牙。
- CarLink 运行时 YU7 不接受蓝牙音乐，因此 `通过 CarLink 播放音频` 必须保持开启。
- 已在 Xiaomi YU7 Max 上测试。车辆偶尔仍会断开蓝牙，此时重复第 2–4 步。

## 用你的语言使用车机助手

车机助手（超级小爱）只听得懂中文。XiaoDroidLink 为其他语言的用户转述：用户用自己的语言说出指令，手机**用自己的扬声器**以中文复述，车辆执行。可以控制空调、座椅、车窗、前备箱、雨刮、灯光和屏幕主题。

支持用乌克兰语、俄语、英语、法语和西班牙语说指令，从 7.67 起还支持德语、波兰语、哈萨克语、阿塞拜疆语、乌兹别克语、塔吉克语、格鲁吉亚语、亚美尼亚语和吉尔吉斯语。这九种语言的指令已翻译，但尚未在车上测试。

如果你会说中文，直接对车机助手说就行，不需要这个功能。应用语言为中文时，手机会把听到的中文原样转述。

### 开启

1. 手机上：XiaoDroidLink → 设置 → 打开 **“用你的语言使用车机助手”** 开关。
2. 如果手机询问，允许使用麦克风。
3. 手机需要中文语音合成（Samsung 和 Google 一般自带）。如果没有，车机屏幕会提示：设置 → 文字转语音 → 安装中文。

开关关闭时，方向盘语音按钮仍和以前一样打开手机 AI（在“麦克风按钮”中选择的 ChatGPT、Gemini 或系统助手）。

### 使用

![语音按钮：按下方向盘左侧辐条上的滚轮](images/steering-wheel-assistant.png)

1. **按下方向盘左侧滚轮**（是按下，不是滚动）。车机助手被唤醒，手机同时开始聆听，车机屏幕显示“请说出要车辆做什么…”。
2. 用应用语言说出指令。
3. 约 3 秒后，手机用中文说出指令，车辆执行并用中文回答。如果手机没有识别出指令，车机屏幕显示“没听懂：…”。

说“人工智能”、“AI”、“ChatGPT”或“Gemini”可打开**手机 AI**：手机先让车机助手退出（“退出小爱”），再打开 AI。

**语音打电话：** 按方向盘按键，说“打电话给王芳”或“给妈妈打电话”。手机在通讯录中查找姓名并拨打；有多个匹配时，车机屏幕最多列出三个供选择。首次使用需在手机上允许访问通讯录。车机蓝牙未连接时手机不会拨打（否则通话会走手机扬声器），而是打开车辆选择并提示重新拨打。

**屏幕上的指令列表：**车机上点齿轮 → **“🗣 助手指令”**（设置顶部）；手机上在“用你的语言使用车机助手”开关下方点 **“助手指令”**。列表只包含已在车上验证的指令，以及车辆无法语音控制的功能。

### 支持的指令

已在车上验证：温度调高、调低，温度调到指定度数；空调开、关；座椅加热（可加“驾驶员”“乘客”或“后排”）、通风、按摩；方向盘加热；后窗除霜；前挡除雾；后视镜加热、折叠、展开；车窗开、关、开一半、开条缝；前备箱开、关；后备箱开、关；充电口开、关；雨刮、雨刮洗涤；车内灯开、关；后雾灯；氛围灯颜色（如红色、蓝色）；浅色、深色模式；音量调到指定数值；雪地模式（车辆会确认）。远光灯无法语音控制，请使用左侧拨杆，手机会提示。

这里只列出 2026 年 10 月 25–27 日在车上验证过的指令。手机还能转述更多指令（悬架、能量回收、收音机），仍在测试中，验证后会补充到这里。是否执行由车辆决定：部分操作可能只在驻车时允许。

### 限制

- 必须使用**方向盘按钮**。手机无法用“小爱同学”唤醒车机助手：车机只会短暂闪烁，不继续聆听（所有语音唤醒设置都试过）。
- 手机需放在**车内**（充电座或支架上），不要放在口袋或包里：车辆需要听到手机扬声器的声音。

## 建议设置

- 使用 Google Maps 或手机屏幕模式时保持手机解锁。
- 如果需要仪表盘地图，打开 Google Maps in the dashboard。可在 Dashboard map app 中选择 Waze 或其他已安装地图应用。
- 只有当车辆无法接收蓝牙音频时，才打开 Audio through CarLink。
- 在 Apps in the car 中添加需要的应用。
- 第一次成功连接后，可以保持 Auto-connect 开启。

## 常见问题

手机和车机屏幕上全部提示的完整列表及设置截图（英文）：[屏幕错误与解决方法](TROUBLESHOOTING.md)。

### 找不到车辆

- 先在车机屏幕上打开 CarLink。
- 关闭车机上的 CarLink，然后重新打开。
- 在手机上关闭并重新打开 Bluetooth。
- 确认已授予 location 权限。
- 将手机靠近车辆。

### 验证码不被接受

- 输入车机屏幕上最新的验证码。
- 如果验证码已变化，请输入新的验证码。
- 关闭并重新打开车机上的 CarLink。
- 点击 Disconnect，然后重新开始。

### 车辆 Wi-Fi 无法连接

- 连接过程中保持车机上的 CarLink 打开。
- 关闭 VPN，或把 XiaoDroidLink 加入 VPN 例外。
- 在手机上关闭并重新打开 Wi-Fi。
- 如果手机连接到旧网络，请忘记旧的车辆 Wi-Fi 网络。

### 屏幕投射无法开始

- Android 请求权限时选择 Entire screen。
- 保持手机解锁。
- 确认 XiaoDroidLink 没有电池限制。
- 关闭并重新打开应用。

### 车机触摸无效

- 在 Android 无障碍设置中启用 XiaoDroidLink。
- 如果 Android 阻止此选项，请在应用信息页面允许 restricted settings。
- 启用无障碍后断开连接并重新连接。

### 音乐控制无效

- 授予 XiaoDroidLink notification access。
- 在手机上开始播放音乐。
- 检查 Music button player 设置。
- 授予通知权限后重新打开 XiaoDroidLink。

### 声音仍从手机播放

- 将手机连接到车辆蓝牙。
- 如果蓝牙音频不可用，打开 Audio through CarLink。
- 更改音频设置后断开并重新连接。

### 地图不显示

- 打开 Google Maps in the dashboard。
- 允许屏幕投射。
- 保持手机解锁。
- 在手机上启动所选地图应用的导航。

### 后台连接中断

- 关闭 XiaoDroidLink 的电池限制。
- 不要强制关闭应用。
- 保持活动连接通知。
- 如果手机有自带电池管理器，把 XiaoDroidLink 加入白名单。

## 诊断日志

应用内：

```text
Diagnostics -> Show log
```

手机文件：

```text
Android/data/salon.lifestyle.xiaodroidlink/files/probe.log
```

## Support

支持：xiaodroidlink@lifestyle.salon
