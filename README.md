# Graduation Thesis Skill

用于中文本科毕业论文写作的 Codex Skill。它面向“真实项目源码 + 开题报告/任务书 + 学校格式手册 + Word 说明书”的毕业设计场景，帮助 AI 完成论文大纲、正文写作、图表制作、Word 回写、格式检查、AIGC 检测报告处理和降 AIGC 改写。

## 项目内容

- `SKILL.md`：Skill 主入口，包含触发说明、总规则和主流程。
- `references_env/`：AI 使用前的最小环境检查。
- `references_diagram/`：论文图片、流程图、类图、E-R 图等制作规则。
- `reference-images/`：各类论文图片的参考示例。
- `references_format/`：根据学校手册、模板、示例论文生成 `论文格式.md` 的规则。
- `references_word/`：Word 回写、备份、格式修改和交付检查规则。
- `references_aigc/`：AIGC 检测报告处理、降 AIGC 工具使用和验收规则。
- `tools/BypassAIGC/`：内置降 AIGC 辅助工具运行包。

## 参考项目

- BypassAIGC：[https://github.com/chi111i/BypassAIGC](https://github.com/chi111i/BypassAIGC)
- BypassAIGC exe 源码：[https://github.com/xyy54323/BypassAIGC](https://github.com/xyy54323/BypassAIGC)

## 最小环境

基础使用需要：

1. Windows 系统。
2. Codex 或支持本地 Skill 的 AI 客户端。
3. Microsoft Word 或 Office，用于 `.docx` 回写、目录、页码和交叉引用检查。
4. Python 3，用于文档、图片和辅助检查脚本。
5. PowerShell，用于本地文件操作、备份和 Word COM 调用。

按需安装：

- draw.io Desktop：需要制作或导出 `.drawio` 图片时安装。下载地址：[draw.io Desktop](https://github.com/jgraph/drawio-desktop/releases/latest)。
- Playwright：需要运行项目页面并截图时使用。
- 项目运行环境：只有需要运行真实项目截图时才安装，如 Java、Maven、Node.js、npm、MySQL 等。

## 安装方式

将仓库克隆到 Codex 的 skills 目录，例如：

```powershell
git clone https://github.com/xyy54323/Graduation-Thesis-skill.git "$env:USERPROFILE\.codex\skills\graduation-thesis-skill"
```

重启 Codex 后，确认 skill 列表中能看到 `graduation-thesis-skill`。

如果只在当前项目中使用，也可以把本仓库放在任意工作目录下，再在对话中显式引用 `SKILL.md`。

## AIGC 工具配置

降 AIGC 功能使用：

```text
tools/BypassAIGC/AI学术写作助手.exe
```

该 exe 对应源码参考：[https://github.com/xyy54323/BypassAIGC](https://github.com/xyy54323/BypassAIGC)。

运行前确认同目录存在：

```text
AI学术写作助手.exe
.env
ai_polish.db
```

`.env` 需要由用户自己配置真实可用的 API Key、Base URL 和模型名称。仓库中的 `.env` 应保持为模板或占位配置，不要提交真实密钥。

启动后默认访问：

```text
http://localhost:9800
```

有 PaperPass 或 SpeedAI PDF 检测报告时，使用“AIGC片段优化”；没有检测报告时，使用“整篇提取优化”。

## 使用示例

### 生成论文大纲

```text
使用 graduation-thesis-skill，参考项目源码、开题报告和示例论文，生成论文大纲，写入论文大纲.md。
```

### 编写章节正文

```text
使用 graduation-thesis-skill，参考源码和开题报告，写 3.1 系统功能需求，内容写入毕业论文.md。
```

### 制作论文图片

```text
使用 graduation-thesis-skill 和 drawio-skill，制作系统总体架构图，图片放到 assets 目录，并保留 drawio 源文件。
```

### 回写 Word

```text
使用 graduation-thesis-skill，参考论文格式.md，把毕业论文.md 中的第 4 章回写到毕业设计说明书.docx。
```

### 根据检测报告降 AIGC

```text
使用 graduation-thesis-skill，根据 PaperPass/SpeedAI PDF 检测报告和原始 docx，启动内置工具进行 AIGC片段优化，导出后立即恢复正文参考文献引用跳转，并生成降AIGC分析报告.md 和 降AIGC修改说明.md。
```
