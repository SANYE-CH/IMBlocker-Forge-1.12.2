# IMBlocker Forge 1.12.2 Community Edition

这是基于 [IMBlocker](https://github.com/reserveword/IMBlocker) 复刻的独立 Forge 1.12.2 客户端模组。

本项目不属于官方 IMBlocker 主线，也不代表官方仓库的合并版本。它面向仍在使用 Minecraft 1.12.2 的玩家，由社区独立维护。

## 当前状态

这是测试版本。已使用 Minecraft 1.12.2、Forge 14.23.5.2860 和 Java 8 完成构建验证，但不同启动器、Windows 版本及第三方输入法仍需要分别测试。

## 功能

- Forge 1.12.2 LaunchWrapper CoreMod 加载。
- 聊天框、命令输入、创造模式搜索、铁砧、服务器列表、书本、告示牌和命令方块等原版文本界面支持。
- Windows IMM32 输入法控制，包含微软拼音、搜狗、讯飞、QQ 拼音、百度输入法、Rime 等兼容目标。
- 普通文本框保留 Shift 手动切换能力。
- 非文本界面解除 HIMC，避免输入法快捷键影响游戏。
- 命令输入英文状态锁定、窗口重新激活恢复和低频状态校验。
- 候选框位置同步和输入法上下文恢复。

## 安装

1. 使用 Java 8 创建 Minecraft 1.12.2 Forge 实例。
2. 将构建生成的 JAR 放入该实例的 `mods` 文件夹。
3. 启动后检查日志中是否出现 `IMBlockerLoadingPlugin` 和 `imblocker`。

## 构建

```text
gradlew.bat clean build --no-daemon --console plain
```

构建产物位于 `build/libs/`。

## 配置

配置文件位于 Forge 的 `config/imblocker.cfg`。Windows 状态监测相关配置：

```text
watchdogEnabled=true
watchdogIntervalTicks=5
watchdogCooldownMs=150
```

如果输入法不响应转换状态 API，可以使用：

```text
englishStateMode=DISABLE_IM
```

## 免责声明

请在使用前备份游戏实例。该项目为独立社区复刻项目，问题反馈和后续维护请提交到本项目，不要默认提交到官方 IMBlocker 仓库。
