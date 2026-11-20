# knowledge-base-curation

通用知识库整理 Skill。用于从书籍、文章、讲义、问答、笔记或可核实的视频文字稿提取知识，审查既有条目，提交稿件及合入已批准的内容。例子和演示数据均为虚构。

## 开始使用

1. 在支持 Agent Skills 的环境中添加 [knowledge-base-curation](knowledge-base-curation/) 目录，并确认可以读取 [SKILL.md](knowledge-base-curation/SKILL.md) 和其引用文件。
2. 从 [接入配置模板](knowledge-base-curation/references/config-template.md) 复制一份表，填写自己的规则位置、库结构、正文和出处的位置、字段与状态映射及确认方式。真实库链接和私有配置保留在自己的环境。
3. 交给智能体材料、配置和任务范围。设定只读审查、整理提交或合入获批项中的一种。平台能访问目标知识库时，Skill 才能核对实况。写入还取决于连接器权限和用户当次授权。

任务示例：「用 knowledge-base-curation 读取附件与我的接入配置。审查这些条目，给我可粘贴的修订稿。」「把提案 2.1 的 A01 和 A03 合入，逐项读回确认。」

没有 Skill 安装入口的环境可直接把 SKILL.md 和本次需要的参考文件提供给智能体，也用同样的配置和任务范围调用。

## 安装和版本更新

- **支持 Agent Skills 的运行时**：添加内层的 knowledge-base-curation 目录。识别结构及维护说明请参阅 [Agent Skills 规范](https://agentskills.io/specification)和 [OpenAI Skills 文档](https://developers.openai.com/plugins/concepts/skills)。
- **Claude 文件导入**：参照官方 Custom Skills 上传说明。如需上传专用 ZIP，将内层 knowledge-base-curation 目录单独压成 ZIP，使目录处于压缩包顶层。[Claude 官方文档](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- **GitHub 维护**：把本发布包中的 README、CHANGELOG 和内层 Skill 目录放在仓库根目录。更新时核对引用、运行样例、更新变更记录并发布版本标签。按目标平台的接入方式更新已部署副本；文件导入方式更新时使用该版本的文件。

该文件包使用通用 Skill 格式。具体平台内的安装和生产库连接需要使用者按自己的环境验证。
