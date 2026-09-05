# burn-humanizer

**有分寸的拟人化。** 少一点铺陈和说教，抓住值得讲的细节，知道什么时候停。

由 **burn** 维护的文本与视觉编辑技能。适用于中文和中英混排的文章、口播、文档、幻灯片、网页与配图。

## 它关心什么

AI 感不只来自套话，也来自一种过度热心：一个小问题，附上一整套背景、框架、例外和总结。

burn-humanizer 先做取舍。回应眼前的问题，保留有用或有趣的细节，删除只是证明自己很周全的部分。然后再调整句子、阅读层级、字体、颜色和图文关系。

它保留事实、作者声音和指定风格。不编个人经历，不强行幽默，不把所有作品改成同一套极简模板。用户需要长文或完整论证时，仍然充分完成。

## 使用

```text
$burn-humanizer 改一下这段话。别展开成教程，保留我原来的意思。

$burn-humanizer 把这篇文章写得自然一点，抓住材料里有意思的地方，不编故事。

$burn-humanizer 调整这份 PPT 的文字和视觉层级，保留品牌色。
```

只想改文字，可以加一句“只改正文，不改格式”。有自己的文章或设计样本，也可以一起提供。

## 安装

下载或克隆本仓库，将完整文件夹命名为 `burn-humanizer`，放入所用工具的 skills 目录。保留 `references` 和 `agents` 子目录，不要只复制 `SKILL.md`。

- Codex 全局：`~/.codex/skills/burn-humanizer/`
- Codex 项目：`项目/.codex/skills/burn-humanizer/`
- Claude Code：`~/.claude/skills/burn-humanizer/`

从旧版 `humanizer-zh` 迁移时，先备份并移出旧技能目录，再使用新名字调用，避免两份规则同时触发。

## 来源与许可

本项目基于 [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh) 扩展重写，原项目源自 [blader/humanizer](https://github.com/blader/humanizer)，并参考 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)。本项目由 burn 独立维护，不是上游官方版本。

采用 [MIT 许可证](LICENSE)，保留原作者版权声明。新增内容包括篇幅与注意力取舍、平等语气、趣味细节，以及多维视觉编辑和行为评估。

当前版本：**2.1.0**。这些规则用于改善作品，不用于判定作者身份或保证 AI 检测分数。结构校验与编辑自检不等于真实读者盲评；行为案例见 [evaluation.md](references/evaluation.md)。
