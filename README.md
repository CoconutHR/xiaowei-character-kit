# 小微拟人化角色创作工具包（非官方社区项目）

> 以标准参考图、角色规范、提示词与 Agent Skill，帮助创作者复现小微的视觉形象，并进行插画、表情、漫画与应用素材二创。
>
> **非官方声明：** 本项目是社区创作，不代表微信、腾讯或任何模型平台的官方形象、立场或背书。许可不授予第三方商标、品牌标识或其他非维护者控制的权利。

[GitHub 仓库](https://github.com/CoconutHR/xiaowei-character-kit) · [角色规范](CHARACTER_SPEC.md) · [素材索引](assets/reference/README.md) · [提示词包](prompts/xiaowei-character-prompt-kit.md) · [贡献指南](CONTRIBUTING.md) · [许可说明](LICENSE-CONTENT-DECISION.md)

<p align="center">
  <img src="assets/avatars/xiaowei-avatar-v1.png" alt="小微非官方拟人头像" width="280">
</p>

## 当前已包含

- **11 张原始 PNG**：母图、三视图、细节板、12 格表情板、8 格动作板、6 格助手状态板、9 格贴纸草案、头像、透明单角色、主题插画与 8 项道具板。
- **12 组提示词与单张贴纸模板**：保留初始设计流程，并补充现有素材引用与母图优先规则。
- **可独立安装的角色 Skill**：自带母图、简明规范和许可声明；无需仅凭文字猜测角色外观。
- **素材清单**：[assets/manifest.json](assets/manifest.json) 记录原文件名、用途、尺寸、SHA-256、透明像素、参考版本、来源、许可和已知偏差。

## 快速开始：复现现有小微

先下载仓库 ZIP，或克隆项目：

```bash
git clone https://github.com/CoconutHR/xiaowei-character-kit.git
```

1. 上传 [母图](assets/reference/xiaowei-master-v1.png) 作为图像参考。复现现有角色时，不要重新用 Prompt 01 生成另一张母图。
2. 按任务补充 [三视图](assets/reference/xiaowei-turnaround-v1.png) 或 [细节板](assets/reference/xiaowei-details-v1.png)，最多先加一张辅助图；冲突时以母图为准。
3. 从 [提示词包](prompts/xiaowei-character-prompt-kit.md) 选择任务模板；新动作与场景优先使用 Prompt 12。
4. 明确输出数量、动作、比例、背景及是否需要透明；保留发型、眼睛、服装、发夹、挎包和星星锚点。
5. 根据 [角色验收清单](CHARACTER_SPEC.md#每张新图的验收清单) 检查结果；分享时标注来源、CC BY 4.0 和修改情况。

图像参考比重复文字描述更重要。提示词不能保证不同模型、种子或轮次像素级复现。

## 素材概览

| 分类 | 文件 | 用途 / 状态 |
|---|---|---|
| 标准参考 | [母图](assets/reference/xiaowei-master-v1.png) | 1672 × 941；身份锚点，带白色贴纸光晕 |
| 标准参考 | [三视图](assets/reference/xiaowei-turnaround-v1.png) / [细节板](assets/reference/xiaowei-details-v1.png) | 各 1254 × 1254；辅助设定，母图优先 |
| 表情 | [表情板](assets/expressions/xiaowei-expression-sheet-v1.png) | 4 列 × 3 行；未拆分 |
| 动作 | [动作板](assets/actions/xiaowei-action-sheet-v1.png) | 4 列 × 2 行；未拆分 |
| 助手状态 | [状态板](assets/actions/xiaowei-assistant-state-sheet-v1.png) | 3 列 × 2 行；未拆分，状态以实际画面为准 |
| 贴纸 | [九宫格草案](assets/stickers/xiaowei-sticker-draft-sheet-v1.png) | 3 列 × 3 行；非平台验收成品 |
| 头像 | [头像概念图](assets/avatars/xiaowei-avatar-v1.png) | 方形画布，圆形构图；未导出多尺寸图标 |
| 单角色 | [透明单角色](assets/characters/xiaowei-character-isolated-v1.png) | 独立全身 PNG；需检查残留白边与阴影 |
| 插画 | [主题插画](assets/illustrations/xiaowei-key-illustration-v1.png) | 实际是方形透明插画，不是横版 16:9 启动页 |
| 道具 | [道具板](assets/props/xiaowei-prop-sheet-v1.png) | 4 列 × 2 行；未拆分 |

除母图外，当前图片均为 **1254 × 1254**。所有图片含真实透明像素，但透明通道不等于无描边、无阴影或已完成边缘清理。本次仅原样复制素材，未裁切、重绘、拆分或放大。

## 安装角色 Skill

在仓库根目录执行：

```bash
mkdir -p ~/.codex/skills
cp -R skills/xiaowei-image-character ~/.codex/skills/
```

重开会话后按环境规则调用 `xiaowei-image-character`（Codex 中可使用 `$xiaowei-image-character`）。安装包自带 `references/xiaowei-master-v1.png`，仅复制 Skill 文件夹仍可读取母图。

Skill 负责选择参考图、写提示词和检查角色一致性，不自带模型服务、API 凭据或生图执行程序。能否直接生成图片取决于当前环境；不能生成时，应返回可复制提示词。其他 Agent 的安装目录以相应工具说明为准。

## 目录结构

```text
assets/
  reference/       母图、三视图、细节板与完整素材索引
  expressions/     表情参考板
  actions/         动作与助手状态参考板
  stickers/        贴纸草案
  avatars/         头像概念图
  characters/      单角色素材
  illustrations/   主题插画
  props/           道具参考板
  manifest.json    机器可读素材元数据
prompts/           提示词包与使用说明
skills/            可安装的角色创作 Skill
.github/           Issue 与 PR 模板
CHARACTER_SPEC.md   角色规范 v1
CONTRIBUTING.md     社区贡献规则
LICENSE            CC BY 4.0 正式全文
LICENSE-CODE-MIT.txt
LICENSE-CONTENT-DECISION.md
THIRD_PARTY_NOTICES.md
```

## 许可：允许二创与商业使用

**图片、角色规范、提示词、说明文档及 Skill 说明文本：CC BY 4.0。** 可复制、修改、分发和商业使用；需适当署名、附许可链接并说明修改。不要求二创使用相同许可证，也不要求二创者公开工具源码。对原有 CC BY 内容仍须保留许可与署名，不得施加妨碍接收者行使该许可权利的附加限制。

**独立工具代码、脚本及配套配置：MIT。** 当前不包含生图执行器；MIT 不替代图片和说明文本的 CC BY 许可。未来如加入第三方素材，应逐项标明其自身许可。

建议署名格式：

> 小微角色创作工具包，项目维护者与贡献者，CC BY 4.0（https://creativecommons.org/licenses/by/4.0/）。来源：https://github.com/CoconutHR/xiaowei-character-kit 。修改：按实际填写；未修改时可写“未修改”。

使用时保留实际项目来源地址，新增作者的署名方式以素材记录为准。署名中的维护者与贡献者指本项目，而非微信、腾讯或模型供应商。

完整法律条款见 [LICENSE](LICENSE)，授权范围与记录见 [许可决策](LICENSE-CONTENT-DECISION.md)；第三方品牌及 AI 素材边界见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。这些声明不保证素材在所有司法辖区具有排他性著作权，也不授予第三方商标权或官方身份。

## 社区参与与后续方向

欢迎贡献表情、动作、漫画、服装变体、提示词适配和工具。角色一致性要求是**本仓库接收标准**，不是限制社区改编的额外许可条件；不同风格或重新设计可标注为变体并独立发布。

初始素材库已经完整收录。下一步可按实际需要拆分图板、清理副本边缘、导出多尺寸图标与横版插画，并为新生成素材记录完整参数。项目通过 [GitHub Issues](https://github.com/CoconutHR/xiaowei-character-kit/issues) 收集反馈，并通过 Pull Requests 接收贡献。公开仓库不包含维护者的本地工作记录或交付压缩包。
