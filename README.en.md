<div align="center">

English | [简体中文](README.md)

</div>

# X-WIDE

I build plugins for ComfyUI and DeepSeek Harness. I like solving small, concrete problems properly: say why it happens first, then ship a fix you can verify.

<p align="center">
  <img src="https://raw.githubusercontent.com/XWIDE/dsh-picflow/main/assets/screenshot-1.png" alt="dsh-picflow: the reference-material panel next to the composer, thumbnails ordered by number, with day filters and an auto-insert switch" width="720">
</p>

## DeepSeek Harness plugins

| Plugin | In one line |
| --- | --- |
| [dsh-picflow](https://github.com/XWIDE/dsh-picflow) | **Pasted screenshots become numbered references.** Every `Ctrl+V` image goes into the official attachment library and gets a stable number (`图片N`), shows up in a panel next to the composer, and can be inserted as a reference chip from the `@` menu — automatically at the caret when the auto-insert switch is on. |
| [dsh-draft-keeper](https://github.com/XWIDE/dsh-draft-keeper) | **The image you pasted is still there after you switch conversations and come back.** It mirrors image drafts per session in the browser and hands them back through the official draft channel when the composer remounts; it forgets them the moment the message is sent or you remove them. |

```sh
# install into this machine's profile (DSH desktop app / dsh web)
curl -fsSL https://raw.githubusercontent.com/XWIDE/dsh-picflow/main/install.sh | sh
curl -fsSL https://raw.githubusercontent.com/XWIDE/dsh-draft-keeper/main/install.sh | sh
```

Both are "client half + thin host half", with no build step and no runtime dependencies; restart whatever hosts the plugin afterwards.

## ComfyUI plugins

| Plugin | In one line |
| --- | --- |
| [comfyui-x-wide-plugin-model-manager](https://github.com/XWIDE/comfyui-x-wide-plugin-model-manager) | What slows down startup · what depends on what · what breaks if you touch it · which models nobody uses |
| [comfyui-xwide-use-everywhere](https://github.com/XWIDE/comfyui-xwide-use-everywhere) | Fixes cg-use-everywhere's browser-side wires (the flowing lines) not rendering — a fixed fork under Apache-2.0 |
| [comfyui-x-wide-image-latent-sender-receiver](https://github.com/XWIDE/comfyui-x-wide-image-latent-sender-receiver) | Image and latent sender / receiver nodes for ComfyUI (bilingual UI) |
| [comfyui-preset-switch-plus](https://github.com/XWIDE/comfyui-preset-switch-plus) | Save a whole workflow's state as several presets and switch them in one click (node modes and widget values together) |

## How these repos are written

- They open with **one line**: what it solves and why it needs to exist.
- **Limits are written as clearly as features**: what it cannot do, and what it costs, is in the README instead of being left for you to discover.
- **Tests are runnable**: every plugin's `tests/` holds plain `.mjs` files — `node tests/xxx.mjs` prints the result.

<p align="center">
  <a href="https://space.bilibili.com/374064919">bilibili</a>
</p>
