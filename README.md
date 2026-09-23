# Implement from Figma

参考图处理技能合集，包含两个可独立安装的技能。

| 技能目录 | 用途 | 调用方式 |
| --- | --- | --- |
| [image-to-prompt](./image-to-prompt/) | 分析参考图的主体、构图、风格、光色与材质，输出完整反推及优化生图提示词 | `$image-to-prompt` |
| [reference-to-figma](./reference-to-figma/) | 将界面参考图还原为可编辑 Figma 图层，识别风格、重建清晰图标并进行整页视觉验收 | `$reference-to-figma` |

## 安装

下载或克隆本仓库，将需要的技能文件夹复制到你的 Codex 技能目录。可同时安装两个技能，保持各自的 SKILL.md、agents 和 references 目录结构完整；不要将整个仓库作为一个技能安装。若目标已存在同名技能，先备份再替换。

重新开启任务后，输入技能名称并附上参考图即可调用。

## 使用示例

- `使用 $image-to-prompt 分析这张参考图，输出视觉拆解、完整反推提示词和优化版提示词。`
- `使用 $reference-to-figma 将这张参考图还原到这个 Figma 文件中，保持文字与普通图标可编辑。`

Figma 还原需要可用的 Figma 工具连接及目标文件编辑权限。复杂插画可根据用户选择保留为独立图片层；图片内部不具备矢量可编辑性。字体、参考图清晰度和工具能力可能影响还原效果，不承诺未经验证的还原百分比。

## 文件说明

两个子目录是对应技能的完整源文件。根目录的 SKILL.md、agents/、references/ 保留作为早期 reference-to-figma 安装方式的兼容副本；新安装请使用上表中的独立技能目录。

[Implement from Figma.skill](./Implement%20from%20Figma.skill) 是 reference-to-figma 的打包文件，不包含 image-to-prompt。
