<div align="center">

[English](README.en.md) | 简体中文

</div>

# X-WIDE

做 ComfyUI 与 DeepSeek Harness 的插件。喜欢把一个小而具体的问题解决干净：先说清它为什么会发生，再给出能验证的修法。

<p align="center">
  <img src="https://raw.githubusercontent.com/XWIDE/dsh-picflow/main/assets/screenshot-1.png" alt="dsh-picflow：输入框旁的「引用素材」面板，缩略图按编号排列，带按天筛选与「自动插入」开关" width="720">
</p>

## DeepSeek Harness 插件

| 插件 | 一句话 |
| --- | --- |
| [dsh-picflow](https://github.com/XWIDE/dsh-picflow) | **粘贴的截图按编号引用。** 每一次 `Ctrl+V` 的图都收进官方附件库、拿到固定编号（`图片N`），列在输入框旁的面板里，可经 `@图片` 菜单插入引用芯片；开着「自动插入」时粘贴后直接落到光标处。 |
| [dsh-draft-keeper](https://github.com/XWIDE/dsh-draft-keeper) | **切走对话再回来，你刚粘进输入框的那张图还在。** 按会话把图片草稿镜像在浏览器里，输入框重新挂载时经官方草稿通道放回去；消息一发出、或你手动删掉，就立刻忘掉。 |

```sh
# 装到本机（DSH 桌面端 / dsh web 的 profile 里）
curl -fsSL https://raw.githubusercontent.com/XWIDE/dsh-picflow/main/install.sh | sh
curl -fsSL https://raw.githubusercontent.com/XWIDE/dsh-draft-keeper/main/install.sh | sh
```

两个都是「客户端半边 + 轻宿主半边」，无构建步骤、无运行时依赖；装完把承载插件的应用重启一次。

## ComfyUI 插件

| 插件 | 一句话 |
| --- | --- |
| [comfyui-x-wide-plugin-model-manager](https://github.com/XWIDE/comfyui-x-wide-plugin-model-manager) | 谁在拖慢启动 · 谁被谁依赖 · 动了谁会坏 · 哪些模型没人用 |
| [comfyui-xwide-use-everywhere](https://github.com/XWIDE/comfyui-xwide-use-everywhere) | 修复 cg-use-everywhere 浏览器端连线（流动线）不显示的问题 —— Apache-2.0 的修复版 fork |
| [comfyui-x-wide-image-latent-sender-receiver](https://github.com/XWIDE/comfyui-x-wide-image-latent-sender-receiver) | 图片和潜空间收发：ComfyUI 独立的图像与潜空间收发节点（中英双语界面） |
| [comfyui-preset-switch-plus](https://github.com/XWIDE/comfyui-preset-switch-plus) | 把整个工作流的状态存成几套预设，点一下整体切换（开关状态与参数值一起切） |

## 这些仓库的写法

- **一句话**开头：它解决什么，为什么需要它。
- **边界写得和功能一样清楚**：做不到什么、代价是什么，写在 README 里，而不是让你事后发现。
- **测试可跑**：每个插件的 `tests/` 都是不依赖框架的 `.mjs`，`node tests/xxx.mjs` 直接出结果。

<p align="center">
  <a href="https://space.bilibili.com/374064919">B 站</a>
</p>
