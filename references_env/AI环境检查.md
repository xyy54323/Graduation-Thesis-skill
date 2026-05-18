# AI环境检查

本文件给 AI 使用，用来判断当前机器和项目资料是否足够支持本 Skill 工作。用户不需要主动操心这些细节；AI 在执行写作、制图、截图或 Word 回写前按需检查即可。

## 必需环境

1. Windows 系统
2. Microsoft Word 或 Office  
   用于打开、回写和检查 `.docx`，以及处理自动目录、页码、交叉引用和分页。
3. Python 3  
   用于处理 Markdown、Word、图片和辅助检查。
4. Python 常用依赖  
   至少准备：`python-docx`、`lxml`、`Pillow`。
5. PowerShell  
   用于文件备份、Word COM 调用和本地脚本执行。

## 按需环境

1. draw.io Desktop 或 drawio-skill  
   需要绘制流程图、类图、架构图、E-R 图时使用。  
   安装链接：
   - 官方下载页：https://www.drawio.com/
   - GitHub Releases：https://github.com/jgraph/drawio-desktop/releases/latest
2. Playwright 或 Playwright CLI Skill  
   需要运行网页、截图后台页面或移动端页面时使用。
3. 项目运行环境  
   只有需要运行项目或截图时才需要，如 Java、Maven、MySQL、Node.js、npm 等。

## 必需资料

1. 真实项目源码
2. 开题报告或项目说明
3. 学校格式手册、模板或示例论文
4. `毕业论文.md`
5. `毕业设计说明书.docx`
6. `assets/` 图片目录
7. `备份/` 分类备份目录

缺少学校格式手册、模板或示例论文时，不能直接确定最终格式，应先在 `论文格式.md` 中标为“待确认”。
