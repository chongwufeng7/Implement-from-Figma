# Implement from Figma

将 UI 参考图、设计稿或截图还原为可编辑 Figma 图层。

技能标识：`reference-to-figma`。本项目处理的是“参考图 → Figma”，不是将 Figma 转换为代码。

## 能力

- 按局部素材识别扁平、线性、渐变、立体、手绘及像素风。
- 保持参考构图、文字与比例，重建可编辑文字、容器和简单矢量图标。
- 复杂插画采用独立图片层，素材方式遵循用户选择。
- 强调图标形状准确、曲线平滑和清晰边缘。
- 对最终 Figma 渲染进行整页走查，发现问题再局部修正；默认不创建额外的图标验收画板。
- 通过复用信息、按需读取和精简工具返回减少重复开销，不降低交付标准。

## 安装

将本仓库克隆到技能目录中名为 `reference-to-figma` 的文件夹。目录内应直接包含 `SKILL.md`、`agents/` 和 `references/`。

在 PowerShell 中指定实际技能目录后执行：

```powershell
git clone https://github.com/chongwufeng7/Implement-from-Figma.git "<技能目录>/reference-to-figma"
```

需要支持技能的执行环境和具有目标文件访问权限的 Figma 工具连接。现有同名技能请先备份并检查，再决定是否替换。

## 使用

附上参考图和目标 Figma 文件链接，然后输入：

> 使用 $reference-to-figma 将这张参考图还原为可编辑 Figma。

无目标文件时，技能会在工具能力允许的情况下创建新文件。完整手机 App 默认采用 402 逻辑宽度及等比高度；其他参考类型不强制套用此尺寸。

## 编辑范围与限制

界面文字、基本布局和简单图标优先保持可编辑。照片和复杂立体插画使用独立位图，内部细节不属于矢量可编辑范围。低分辨率原图、缺失字体或工具限制可能造成差异，交付时应说明。还原度不预设未经验证的百分比。

## 文件

- `SKILL.md`：核心工作流与执行效率规则
- `agents/openai.yaml`：技能展示与调用信息
- `references/construction.md`：布局与复杂素材处理
- `references/icon-quality.md`：图标风格和边缘细则
- `references/visual-review.md`：视觉走查细则

