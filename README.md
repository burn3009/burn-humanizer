# burn-humanizer

一套给 Codex 等支持 skill 的工具使用的中文改稿规则。安装后，把原稿交给模型，用 `$burn-humanizer` 调用。

从 [Humanizer-zh](https://github.com/op7418/Humanizer-zh) 改来。除了检查套话，也处理重复解释、篇幅和语气；文档、幻灯片或网页还可以检查排版与配色，需要相应的编辑工具配合。

## 例子

比如这句通知：

> 为了确保后续工作的顺利开展，请各位同学务必于周五前提交草图和材料清单，为接下来的创作做好充分准备。

可以改成：

> 请各位同学于周五前提交草图和材料清单。

时间和要交的东西都留下了，前后的铺垫没有必要。如果原文已经写得清楚，就不必改。小说、评论或个人随笔也不能照这个例子一味删短。

## 安装

下载本仓库，把完整的 `burn-humanizer` 文件夹放到 skills 目录。`SKILL.md`、`references` 和 `agents` 要一起保留。

| 工具 | 目录 |
| --- | --- |
| Codex，全局使用 | `~/.codex/skills/burn-humanizer/` |
| Codex，仅当前项目 | `项目/.codex/skills/burn-humanizer/` |
| Claude Code | `~/.claude/skills/burn-humanizer/` |

装过旧版 `humanizer-zh` 的话，先把旧文件夹移到 skills 目录之外备份，避免两套规则同时生效。

## 使用

在 Codex 中输入：

```text
$burn-humanizer 修改下面这段话，保留原意：

[粘贴原文]
```

也可以提供文件。只想改文字，就写“只改正文，不动格式”。如果有自己的旧稿，可以一起提供作为参考；比“写得像真人”更容易让模型知道你想保留什么。

目前还没有做读者盲评，不能承诺改稿一定更好。规则和检查案例都在仓库里，具体怎么判断可看 [evaluation.md](references/evaluation.md)。对这份 README 的一次历史文档对照记录见 [readme-study.md](references/readme-study.md)。

## 来源

由 burn 维护，采用 [MIT 许可证](LICENSE)，保留原作者版权声明。

基于 [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh) 扩展；上游源自 [blader/humanizer](https://github.com/blader/humanizer)，并参考 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)。这是独立维护的版本。
