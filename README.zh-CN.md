# ModPort Agent Wiki

为 ModPort 研究与编码 Agent 提供按版本区分的迁移知识。

[English](README.md)

本仓库保存针对明确源版本与目标版本组合、可独立于项目记录阅读的研究结论。它是可选的研究资料；条目说明其引用证据和迁移建议，不代表某个项目或 Run 已通过验收。内容复用条款见下方许可说明。

## 从这里开始

根目录的 [index.json](index.json) 列出可用贡献。首个已审核条目覆盖 Java 17 → 25，说明选择 `List.get(0)` 与 `List.getFirst()` 时如何保留空列表的异常行为。条目引用相应版本的 Oracle API 文档；自定义实现和项目运行时行为仍未验证。

在线 ModPort 用户可执行 `modport wiki update`。离线使用时，从 [research-v0.1.0 发布页](https://github.com/FlightDan/modport-wiki-for-agents/releases/tag/research-v0.1.0)下载 `research-v0.1.0.zip`，再执行 `modport wiki import-pack --file /path/to/research-v0.1.0.zip`。这些命令需要包含 Wiki 集成的当前 ModPort 源码；这项应用集成尚未随 ModPort 正式版本发布。

也可以直接阅读索引中的 JSON。上述命令示例供维护者和已有当前 ModPort 源码访问权限的用户使用；请向其维护者取得源码及安装说明。本研究仓库分发知识资料包。

每条索引记录包含贡献 ID、类型、源版本、目标版本和文件路径。打开对应 JSON 文件查看条目及其证据。

| 类型 | 源版本与目标版本字段 |
| --- | --- |
| platform | minecraft、loader、loader_version |
| java | java |

版本值用于说明贡献覆盖的范围。仅有版本信息并不能证明这些版本中的所有功能或运行环境都已检查。

## 如何阅读条目

每个条目包含 ID、类别、摘要、适用范围、迁移建议、兼容性说明、验证说明和证据引用。每条证据引用包含公开 HTTP(S) 来源、来源中的定位信息，以及该来源所支持的结论。

请明确区分证据类型。阅读源码或文档只能支持关于这些来源内容的结论；编译结果只支持所述范围内的编译结论；运行时证据只支持实际执行过的行为。应在条目中直接记录不确定之处，不要把有限结论扩展成某个项目的迁移或验收结论。

## 如何贡献

请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)，并使用[研究工作表](templates/research.md)准备不含私有项目材料的贡献。贡献文件为 JSON，存放在 contributions/platform/ 或 contributions/java/。维护者审核后，会将选定内容纳入带版本的索引和研究资料包。

当前本地 ModPort 已实现可编辑草稿、GitHub CLI 浏览器登录和显式提交 Draft PR。提交使用界面显示的账号及其 fork、分支；上游仓库所有者使用自己的分支。[贡献 #1](https://github.com/FlightDan/modport-wiki-for-agents/pull/1) 已实际验证浏览器授权、所有者账号提交 Draft PR，以及重复提交返回同一个 PR。外部贡献者的 fork 路径、真实模型研究和 Windows 原生行为仍未验证，这项应用集成尚未发布。

维护者按 [贡献说明](CONTRIBUTING.md) 使用本地 `modport wiki build-pack` 命令推广经过审核的材料。在线查询读取发布修订中的版本索引；离线用户可用 `modport wiki import-pack --file FILE` 导入发布的 ZIP 研究包。

## 许可与复用

本文档草案未设定许可条款。复用或再分发贡献内容前，请查看仓库已发布的许可信息并咨询维护者。若仓库未发布许可，复用权限仍未明确。

最后审阅日期：2026-10-07。
