# Image2 重绘 + 原生栅格像素美术 Skill

这是一个可分享的 Codex Skill：先根据目标显示尺寸选像素规格，再用 Image2 等图像工具重绘，之后栅格化到原生网格并逐簇修整，最后检查 1 倍、最近邻放大和实际合成效果。

## 使用

从仓库选择 **Code → Download ZIP** 并解压，将 `image2-pixel-art-workflow` 文件夹复制到项目的 `.agents/skills/` 或个人 Codex Skills 目录。重新打开或刷新 Codex 后，可使用：

`使用 $image2-pixel-art-workflow，把这张参考图重绘并栅格化成像素角色。`

如果不指定规格，Skill 会根据目标用途和显示尺寸给出建议；确实难以选择时，可先用同一主体做少量密度对比。不会把高清图直接缩小后称作完成的像素画。

## 署名授权

本包原始说明文字采用 CC BY 4.0：可以免费使用、修改、再分发，也允许商用；转载或改编时须给出合理署名、链接许可证并说明改动。该许可不要求改编内容也开源。作者署名为 `guantou899`。

许可只覆盖这个 Skill 包本身，不自动覆盖用户参考图、第三方素材或生成的美术资产。完整条款见 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 和仓库 `LICENSE` 文件。
