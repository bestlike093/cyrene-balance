# 素材来源

本插件（Cyrene 插件 `cyrene-balance`，界面上叫「昔涟 · 桌面桌宠」）里的立绘、表情和头像都来自 Cyrene 客户端自带的素材库，没有重新绘制。下面写清每一项的原始位置、处理方式和权利归属。

## 一、取自 Cyrene 客户端素材库

Cyrene 把这些资源打包在安装目录的 `resources/app.asar` 里；同一批文件也在 [Playa-Cyrene/Cyrene-Agent](https://github.com/Playa-Cyrene/Cyrene-Agent) 开源仓库中以相同路径存放，可以直接对照。

| 插件内文件 | 数量 | Cyrene 内原始路径 | 处理方式 |
| --- | --- | --- | --- |
| `assets/frame-01.png` ~ `frame-08.png` | 8 | `assets/ui/cyrene-thinking-loop/frame-01.png` ~ `frame-08.png` | 直接用作姿态立绘 |
| `assets/calm.png`、`confident.png`、`love-happy.png`、`playful.png`、`serious.png` | 5 | `dist/renderer/stickers/` 下同名文件 | 直接用作情绪特写 |
| `assets/emoji/*.png` | 44 | `dist/renderer/stickers/*.jpg`（`Airkiss`、`Allset`、`awesome` … `weeploud`） | 去白底，转成 256×256 透明 PNG |
| `assets/mimi.png` | 1 | `dist/renderer/icons/mimi.png` | 直接用作状态面板头像 |

`assets/DSniang1.png`、`bubble-money1.gif`、`bubble-petpet.gif`、`rua.gif` 是早期版本随插件分发的素材，不在 Cyrene 素材库清单内，也没有可靠的出处记录。

## 二、音效

`greeting.wav`、`cost-default.wav`、`task-end-a.wav`、`minecraft-exp-orb.wav`、`Ya1.mp3`、`Ya2.mp3` 随插件一起分发，不来自 Cyrene 素材库。其中 `minecraft-exp-orb.wav` 按文件名是《Minecraft》的经验球音效，权利归 Mojang；其余音效没有可靠的出处记录。

## 三、角色与授权

- 角色「昔涟」及《崩坏：星穹铁道》的名称、形象、美术与设定归 **HoYoverse / 米哈游** 所有。
- Cyrene 使用的 Live2D 模型（`models/cyrene/`）由 B 站 UP 主 [@是依七哒](https://space.bilibili.com/457683484) 制作，授权范围见 Cyrene-Agent 仓库的 [MODEL_LICENSE.md](https://github.com/Playa-Cyrene/Cyrene-Agent/blob/master/MODEL_LICENSE.md)。本插件只使用静态立绘与贴纸，不包含这个 Live2D 模型。
- 按米哈游同人创作规范，以上素材仅随插件分发，供个人非商业使用，请勿拆分、转售、二次分发或用于商业宣传。

## 四、怎么核对

1. 打开 Cyrene 安装目录下的 `resources/app.asar`，或用 asar 解包工具列出文件，能看到上表里的原始路径。
2. 打开 Cyrene-Agent 仓库，`assets/ui/cyrene-thinking-loop/` 与 `dist/renderer/stickers/` 下有同一批文件。
3. 对比插件 `assets/` 与这两处文件，可以看到只做了透明度与尺寸处理。
