# Stellaris AI recorder

录下你自己玩群星时的操作，用来给 stellaris-ai 网络做模仿学习。这个仓库只发布插件，不含源码。

## 录什么

- 你自己发出的命令（研究、建造、舰队移动、外交等）和你选的事件选项
- 每条命令发出时的游戏日期、你的帝国状态和可选目标，都是触发器算出的 0/1 值

不录 AI 或其他玩家的命令。文件里没有账号、Steam ID、电脑信息或聊天内容以外的个人资料；存档里的帝国名和你的命令参数可能出现在记录中。

插件只把记录写到本地，不会自动上传。要不要发给我们，由你决定。

## 使用要求

- Stellaris **4.5.3**（`stellaris.exe` 构建 `0x6AE49C1B`）。其他版本插件不会启动
- 用 [stellaris-launcher](https://github.com/Yidhar/stellaris-launcher) 启动游戏：只有它会加载这类插件

## 安装

1. 从 [Releases](../../releases) 下载 `stellaris-ai-recorder-v*.zip`，解压到一个文件夹
2. 安装并启动：

```bash
stl plugin install <解压出的文件夹>
```

```bash
stl plugin enable stellaris-ai
```

```bash
stl launch
```

进入一局游戏后就开始录制，正常游玩即可。

## 把记录发回来

记录在：

```
文档\Paradox Interactive\Stellaris\plugins\stellaris-ai\recordings\
```

每次启动游戏生成一个 `.jsonl` 文件。整局完整游玩的记录最有用，开局到中期尤其重要。把文件打包发给联系你的人。

## 关闭录制

把 `plugins\stellaris-ai\config\stellaris_ai.ini` 里的 `record_human=1` 改成 `0`，或者：

```bash
stl plugin disable stellaris-ai
```
