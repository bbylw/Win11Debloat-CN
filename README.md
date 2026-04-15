# Win11Debloat

[![GitHub Release](https://img.shields.io/github/v/release/Raphire/Win11Debloat?style=for-the-badge&label=最新版本)](https://github.com/Raphire/Win11Debloat/releases/latest)
[![加入讨论](https://img.shields.io/badge/加入-讨论-2D9F2D?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Raphire/Win11Debloat/discussions)
[![静态徽章](https://img.shields.io/badge/文档-_?style=for-the-badge&logo=bookstack&color=grey)](https://github.com/Raphire/Win11Debloat/wiki/)

Win11Debloat 是一个轻量级、易于使用的 PowerShell 脚本，旨在帮助你快速清理和自定义 Windows 体验。它可以移除预装的垃圾软件（bloatware）、禁用遥测、移除冗余的界面元素等等。无需再费力地逐一调整设置或手动卸载应用，Win11Debloat 让这一切变得简单高效！

该脚本还包含许多系统管理员和高级用户喜欢的功能，例如强大的命令行界面、支持 Windows 审核模式（Audit mode）以及对其他 Windows 用户进行更改的选项。更多详情请参考我们的 [Wiki](https://github.com/Raphire/Win11Debloat/wiki/)。

![Win11Debloat 菜单](https://github.com/Raphire/Win11Debloat/raw/master/Assets/Images/menu.png)

#### 如果这个脚本对你有帮助，请考虑请我喝杯咖啡以支持我的工作

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M5C6UPC)

## 使用方法

> [!Warning]
> 我们投入了大量精力确保此脚本不会意外破坏任何操作系统功能，但使用风险需自担！如果你遇到任何问题，请在[此处](https://github.com/Raphire/Win11Debloat/issues)提交报告。

### 快速方法

通过 PowerShell 自动下载并运行脚本。

1. 以管理员权限打开 PowerShell 或终端（Terminal）。
2. 将以下命令复制并粘贴到 PowerShell 中：

```PowerShell
& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))
```

3. 等待脚本自动下载 Win11Debloat。
4. 仔细阅读并按照屏幕上的说明操作。

此方法支持通过命令行参数自定义脚本行为。请点击[此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters)了解更多信息。

### 传统方法

<details>
  <summary>手动下载并运行脚本。</summary><br/>

  1. [下载脚本的最新版本](https://github.com/Raphire/Win11Debloat/releases/latest)，并将 .ZIP 文件解压到你喜欢的路径。
  2. 进入 Win11Debloat 文件夹。
  3. 双击 `Run.bat` 文件启动脚本。注意：如果控制台窗口立即关闭且没有任何反应，请尝试下面的高级方法。
  4. 接受 Windows UAC 提示以管理员身份运行脚本（这是脚本运行所必需的）。
  5. 仔细阅读并按照屏幕上的说明操作。
</details>

### 高级方法

<details>
  <summary>手动下载并通过 PowerShell 运行脚本。推荐高级用户使用。</summary><br/>

  1. [下载脚本的最新版本](https://github.com/Raphire/Win11Debloat/releases/latest)，并将 .ZIP 文件解压到指定路径。
  2. 以管理员权限打开 PowerShell 或终端。
  3. 通过输入以下命令临时启用 PowerShell 执行策略：

  ```PowerShell
  Set-ExecutionPolicy Unrestricted -Scope Process -Force
  ```

  4. 在 PowerShell 中，导航到文件解压的目录。例如：`cd c:\Win11Debloat`
  5. 输入以下命令运行脚本：

  ```PowerShell
  .\Win11Debloat.ps1
  ```

  6. 仔细阅读并按照屏幕上的说明操作。

  此方法支持通过命令行参数自定义脚本行为。请点击[此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters)了解更多信息。
</details>

## 功能特性

以下是 Win11Debloat 提供的主要功能概览。有关默认设置预设的更多信息，请参考 [Wiki](https://github.com/Raphire/Win11Debloat/wiki/Default-Settings)。

> [!Tip]
> Win11Debloat 所做的所有更改都可以轻松还原，并且几乎所有的应用都可以通过 Microsoft Store 重新安装。完整的还原指南可以在[此处](https://github.com/Raphire/Win11Debloat/wiki/Reverting-Changes)找到。

#### 应用移除

- 移除各种预装应用。点击[此处](https://github.com/Raphire/Win11Debloat/wiki/App-Removal)查看详情。

#### 隐私与建议内容

- 禁用遥测、诊断数据、活动历史记录、应用启动跟踪和定向广告。
- 禁用 Windows 各处的提示、技巧、建议和广告。
- 禁用 Windows 定位服务和应用位置访问。
- 禁用“查找我的设备”位置跟踪。
- 禁用锁屏界面上的“Windows 聚焦”以及提示和技巧。
- 禁用桌面背景的“Windows 聚焦”选项。
- 禁用 Microsoft Edge 中的广告、建议和 MSN 新闻提要。
- 在设置“主页”中隐藏 Microsoft 365 广告，或完全隐藏“主页”。

#### AI 功能

- 禁用并移除 Microsoft Copilot。
- 禁用 Windows Recall（回忆）。
- 禁用 Click to Do（AI 文本和图像分析工具）。
- 防止 AI 服务 (WSAIFabricSvc) 自动启动。
- 禁用 Edge 中的 AI 功能。
- 禁用画图（Paint）中的 AI 功能。
- 禁用记事本（Notepad）中的 AI 功能。

#### 系统设置

- 禁用用于共享和移动文件的拖拽托盘（Drag Tray）。
- 恢复旧版 Windows 10 风格的右键上下文菜单。
- 关闭“提高指针精确度”（即鼠标加速）。
- 禁用粘滞键（Sticky Keys）快捷键。
- 禁用存储感知（Storage Sense）自动磁盘清理。
- 禁用快速启动以确保完全关机。
- 禁用 BitLocker 自动设备加密。
- 禁用现代待机（Modern Standby）期间的网络连接以减少电池消耗。

#### Windows 更新

- 阻止 Windows 在更新可用时立即获取更新。
- 阻止登录后更新引起的自动重启。
- 禁用与其他电脑共享已下载的更新（传递优化）。

#### 外观

- 为系统和应用启用深色模式。
- 禁用透明效果。
- 禁用动画和视觉效果。

#### 开始菜单与搜索

- 移除或替换开始菜单中所有固定的应用。
- 隐藏开始菜单中的“推荐”部分。
- 隐藏开始菜单中的“所有应用”部分。
- 禁用开始菜单中的“手机连接”移动设备集成。
- 禁用 Windows 搜索中的 Bing 网络搜索和 Copilot 集成。
- 禁用 Windows 搜索中的 Microsoft Store 应用建议。
- 禁用任务栏搜索框中的搜索亮点（动态/品牌内容）。
- 禁用本地 Windows 搜索历史记录。

#### 任务栏

- 将任务栏图标向左对齐。
- 隐藏或更改任务栏上的搜索图标/搜索框。
- 从任务栏中隐藏任务视图按钮。
- 禁用任务栏和锁屏界面上的小组件。
- 从任务栏中隐藏聊天（立即开会）图标。
- 在任务栏右键菜单中启用“结束任务”选项。
- 在任务栏应用区域启用“最后一次活动点击”行为（连续点击图标可切换同一应用的多个窗口）。
- 自定义多显示器环境下任务栏图标的显示方式。
- 选择任务栏按钮和标签的合并模式。

#### 文件资源管理器

- 更改文件资源管理器默认打开的位置。
- 显示已知文件类型的扩展名。
- 显示隐藏的文件、文件夹和驱动器。
- 从导航窗格中隐藏“主页”或“图库”部分。
- 隐藏导航窗格中的重复可移动驱动器条目，仅保留“此电脑”下的条目。
- 将所有常用文件夹（桌面、下载等）重新添加回“此电脑”。
- 从导航窗格中隐藏 3D 对象、音乐或 OneDrive 文件夹。
- 从右键菜单中隐藏“包含在库中”、“授予访问权限”和“共享”选项。
- 更改文件资源管理器中驱动器盘符的位置或可见性。

#### 多任务处理

- 禁用窗口贴靠（Window Snapping）。
- 贴靠窗口时禁用贴靠辅助建议。
- 拖动窗口到屏幕顶部或悬停在最大化按钮上时，禁用贴靠布局建议。
- 更改在贴靠或按 Alt+Tab 时是否显示浏览器标签页。

#### 可选 Windows 功能

- 启用 Windows 沙盒（Windows Sandbox）。
- 启用适用于 Linux 的 Windows 子系统 (WSL)。

#### 其他

- 禁用 Xbox Game Bar 集成和游戏/屏幕录制。
- 禁用 Brave 浏览器中的冗余功能（AI、加密货币、新闻等）。

#### 高级功能

- 支持[对其他用户应用更改](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#running-as-another-user)，而非仅限于当前登录用户。
- [Sysprep 模式](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#sysprep-mode)：将更改应用于 Windows 默认用户配置文件，确保所有新用户都会自动应用这些更改。

## 贡献

我们欢迎各种形式的贡献！请参阅我们的[贡献指南](https://github.com/Raphire/Win11Debloat/blob/master/.github/CONTRIBUTING.md)了解详细的操作说明和最佳实践。

## 许可证

Win11Debloat 采用 MIT 许可证。更多信息请参阅 LICENSE 文件。
