# 标准参考与完整素材索引

## 母图优先

复现现有小微时，先上传 [xiaowei-master-v1.png](xiaowei-master-v1.png)，再按需添加 [三视图](xiaowei-turnaround-v1.png) 或 [细节板](xiaowei-details-v1.png)。辅助图不应覆盖母图身份锚点；尤其检查发夹在角色自身左侧（正面看为观者右侧）及肩带走向。

标准母图不直接覆盖。需要更新时新增版本文件并说明原因。本规则是版本管理约定，不限制 CC BY 4.0 允许的社区改编。

## 11 张原图的来源与用途

所有原图由维护者提供，本次只复制文件，不修改像素。公开署名采用“小微角色创作工具包项目维护者”；内容许可为 **CC BY 4.0**，允许商业使用、改编和分发，需署名、附许可链接及标明修改。正式全文见 [LICENSE](../../LICENSE)，边界说明见 [第三方声明](../../THIRD_PARTY_NOTICES.md)。

| 原文件名 | 项目文件 | 尺寸 | 用途 / 关联模板 |
|---|---|---|---|
| `XiaoWei_Master.png` | [xiaowei-master-v1.png](xiaowei-master-v1.png) | 1672 × 941 | 标准母图 / Prompt 01 为初始概念模板 |
| `标准角色设定三视图.png` | [xiaowei-turnaround-v1.png](xiaowei-turnaround-v1.png) | 1254 × 1254 | 辅助三视图 / Prompt 02 |
| `头部、服装与配件细节板.png` | [xiaowei-details-v1.png](xiaowei-details-v1.png) | 1254 × 1254 | 细节板 / Prompt 03 |
| `面部表情表.png` | [表情板](../expressions/xiaowei-expression-sheet-v1.png) | 1254 × 1254 | 4 列 × 3 行 / Prompt 04 |
| `动作与姿态设定表.png` | [动作板](../actions/xiaowei-action-sheet-v1.png) | 1254 × 1254 | 4 列 × 2 行 / Prompt 05 |
| `AI 助手状态图.png` | [助手状态板](../actions/xiaowei-assistant-state-sheet-v1.png) | 1254 × 1254 | 3 列 × 2 行 / Prompt 06 |
| `九宫格贴纸草案.png` | [贴纸草案板](../stickers/xiaowei-sticker-draft-sheet-v1.png) | 1254 × 1254 | 3 列 × 3 行 / Prompt 07 |
| `头像和应用图标.png` | [头像](../avatars/xiaowei-avatar-v1.png) | 1254 × 1254 | 单图概念 / Prompt 08 |
| `透明背景单角色素材.png` | [透明单角色](../characters/xiaowei-character-isolated-v1.png) | 1254 × 1254 | 单图 / Prompt 09 |
| `主题插画启动画面.png` | [主题插画](../illustrations/xiaowei-key-illustration-v1.png) | 1254 × 1254 | 方形透明插画 / Prompt 10 |
| `原创小道具素材板.png` | [道具板](../props/xiaowei-prop-sheet-v1.png) | 1254 × 1254 | 4 列 × 2 行 / Prompt 11 |

完整的文件哈希、字节大小、透明像素数量、AI 来源及备注见 [assets/manifest.json](../manifest.json)。关联模板只说明创作用途；逐图精确提示词与生成参数未记录，不能声称已逐字复现原图。

## 使用前需要知道

- 所有 PNG 都有真实透明像素；部分带白色贴纸边缘、光晕或阴影，应在目标背景下检查。
- 图板尚未拆分，不能直接当作若干独立 PNG 或均匀动画帧。后续拆分应新增派生文件、保留原图。
- 主题插画不是 16:9 启动画面；头像也未导出多尺寸 / `.ico` / `.icns` 文件。
- 配色表尚未独立取样制作，细节板色块仅是视觉参考。
- 母图宽画布留白较多，不建议直接用整幅画布强制裁成头像；已有独立头像图可用。
- 三视图为 AI 辅助参考，不保证每个视角绝对一致；遇到冲突优先回看母图。

## 署名示例

> 小微角色创作工具包，项目维护者与贡献者，CC BY 4.0（https://creativecommons.org/licenses/by/4.0/）。来源：https://github.com/CoconutHR/xiaowei-character-kit 。修改：按实际填写。

源文件所在的本机个人路径不写入公开素材包。后续贡献请按 [贡献指南](../../CONTRIBUTING.md) 填写各项作者与许可，不沿用“维护者”冒充新作者。
