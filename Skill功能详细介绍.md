# Awesome Claude Skills - 各文件夹功能详细介绍

## 主要Skill文件夹功能说明

### 1. 文档处理类

#### document-skills/docx/
**功能**：全面的Word文档创建、编辑和分析工具
- 支持跟踪更改、评论、格式保留和文本提取
- 创建新文档、修改现有文档、处理跟踪更改
- 适用于法律、学术、商业或政府文档的专业处理

#### document-skills/pdf/
**功能**：PDF操作工具包
- 提取文本、表格、元数据
- 合并/拆分PDF文档
- 处理PDF表单
- 创建新PDF文档

#### document-skills/pptx/
**功能**：PowerPoint演示文稿工具
- 读取、生成和调整幻灯片
- 修改布局和模板
- 支持HTML到PPTX转换

#### document-skills/xlsx/
**功能**：Excel电子表格操作
- 公式和图表操作
- 数据转换和分析
- 电子表格计算和重新计算

### 2. 开发工具类

#### artifacts-builder/
**功能**：HTML构件构建器
- 使用React、Tailwind CSS、shadcn/ui创建复杂的多组件HTML构件
- 适用于claude.ai的视觉效果丰富的网页构件

#### changelog-generator/
**功能**：变更日志生成器
- 分析git提交历史
- 将技术提交转换为客户友好的发布说明
- 自动创建面向用户的变更日志

#### mcp-builder/
**功能**：MCP服务器构建器
- 指导创建高质量的MCP（模型上下文协议）服务器
- 支持Python或TypeScript
- 将外部API和服务与LLM集成

#### skill-creator/
**功能**：技能创建工具
- 提供创建有效Claude Skills的指导
- 包含初始化、打包和验证脚本
- 帮助开发者创建自定义技能

#### webapp-testing/
**功能**：Web应用测试工具
- 使用Playwright测试本地Web应用
- 验证前端功能，调试UI行为
- 捕获屏幕截图

### 3. 商业营销类

#### brand-guidelines/
**功能**：品牌指南应用
- 将Anthropic官方品牌颜色和排版应用于构件
- 实现一致的视觉识别和专业设计标准

#### competitive-ads-extractor/
**功能**：竞争对手广告提取器
- 从广告库中提取和分析竞争对手的广告
- 了解引起共鸣的消息传递和创意方法

#### domain-name-brainstormer/
**功能**：域名创意生成器
- 生成创意域名创意
- 检查多个TLD的可用性（.com、.io、.dev、.ai等）

#### lead-research-assistant/
**功能**：潜在客户研究助手
- 分析产品，搜索目标公司
- 提供可行的外展策略
- 识别和资格认证高质量潜在客户

### 4. 沟通写作类

#### content-research-writer/
**功能**：内容研究和写作助手
- 进行研究，添加引用
- 改进钩子，提供逐节反馈
- 协助撰写高质量内容

#### meeting-insights-analyzer/
**功能**：会议洞察分析器
- 分析会议记录，揭示行为模式
- 识别冲突避免、发言比例、填充词
- 分析领导风格和沟通模式

#### twitter-algorithm-optimizer/
**功能**：Twitter算法优化器
- 使用Twitter开源算法洞察分析推文
- 优化推文以获得最大覆盖率
- 提高参与度和可见性

### 5. 创意媒体类

#### canvas-design/
**功能**：画布设计工具
- 使用设计理念创建PNG和PDF视觉艺术
- 适用于海报、设计和静态作品
- 包含专业字体资源

#### image-enhancer/
**功能**：图像增强器
- 提高图像和屏幕截图的质量
- 增强分辨率、清晰度和清晰度
- 用于专业演示和文档

#### slack-gif-creator/
**功能**：Slack GIF创建器
- 创建为Slack优化的动画GIF
- 具有大小限制验证器
- 可组合的动画原语和模板

#### theme-factory/
**功能**：主题工厂
- 应用专业字体和颜色主题
- 10个预设主题
- 支持幻灯片、文档、报告、HTML登录页面

#### video-downloader/
**功能**：视频下载器
- 从YouTube和其他平台下载视频
- 支持离线观看、编辑或存档
- 支持各种格式和质量选项

### 6. 生产力组织类

#### file-organizer/
**功能**：文件整理器
- 智能组织文件和文件夹
- 理解上下文，查找重复项
- 建议更好的组织结构

#### invoice-organizer/
**功能**：发票整理器
- 自动组织发票和收据
- 读取文件，提取信息
- 一致地重命名，准备税务

#### raffle-winner-picker/
**功能**：抽奖获奖者选择器
- 从列表、电子表格或Google Sheets随机选择获奖者
- 用于赠品和竞赛
- 具有加密安全的随机性

#### tailored-resume-generator/
**功能**：定制简历生成器
- 分析职位描述
- 生成量身定制的简历
- 突出相关经验、技能和成就

### 7. 连接集成类

#### connect/
**功能**：Claude连接器
- 将Claude连接到任何应用程序
- 发送电子邮件、创建问题、发布消息
- 在1000+服务中执行实际操作

#### connect-apps/
**功能**：应用连接插件
- 通过Composio连接到500+应用
- 处理身份验证和应用集成
- 支持Gmail、Slack、GitHub、Notion等

### 8. 其他工具类

#### developer-growth-analysis/
**功能**：开发者成长分析器
- 分析开发者成长数据
- 提供技能改进建议

#### internal-comms/
**功能**：内部通信助手
- 帮助编写内部通信
- 包括3P更新、公司通讯、FAQ等
- 使用公司特定格式

#### langsmith-fetch/
**功能**：LangSmith获取器
- 调试LangChain和LangGraph代理
- 自动从LangSmith Studio获取执行跟踪
- 分析执行跟踪

#### skill-share/
**功能**：技能分享工具
- 分享和管理Claude Skills
- 技能分发和安装

#### template-skill/
**功能**：模板技能
- 提供技能模板
- 帮助快速创建新技能

### 9. Composio自动化技能

#### composio-skills/ (包含78个SaaS应用的自动化技能)
- **CRM和销售**：Close、HubSpot、Pipedrive、Salesforce、Zoho CRM
- **项目管理**：Asana、Basecamp、ClickUp、Jira、Linear、Monday、Notion、Todoist、Trello、Wrike
- **通信**：Discord、Intercom、Microsoft Teams、Slack、Telegram、WhatsApp
- **电子邮件**：Gmail、Outlook、Postmark、SendGrid
- **代码和DevOps**：Bitbucket、CircleCI、Datadog、GitHub、GitLab、PagerDuty、Render、Sentry、Supabase、Vercel
- **存储和文件**：Box、Dropbox、Google Drive、OneDrive
- **电子表格和数据库**：Airtable、Coda、Google Sheets
- **日历和调度**：Cal.com、Calendly、Google Calendar、Outlook Calendar
- **社交媒体**：Instagram、LinkedIn、Reddit、TikTok、Twitter、YouTube
- **营销和电子邮件营销**：ActiveCampaign、Brevo、ConvertKit、Klaviyo、Mailchimp
- **支持和帮助台**：Freshdesk、Freshservice、Help Scout、Zendesk
- **电子商务和支付**：Shopify、Square、Stripe
- **设计和协作**：Canva、Confluence、DocuSign、Figma、Miro、Webflow
- **分析和数据**：Amplitude、Google Analytics、Mixpanel、PostHog、Segment
- **人力资源和人员**：BambooHR
- **自动化平台**：Make (Integromat)
- **Zoom和会议**：Zoom

### 10. 其他项目

#### openskills-main/
**功能**：OpenSkills CLI工具
- 技能管理命令行工具
- 支持安装、列表、管理、读取、移除、同步、更新技能
- TypeScript编写的CLI工具

---

## DOCX技能详细使用文档

### 概述

DOCX技能是一个全面的Word文档创建、编辑和分析工具，支持跟踪更改、评论、格式保留和文本提取。

### 工作流程决策树

#### 读取/分析内容
使用"文本提取"或"原始XML访问"部分

#### 创建新文档
使用"创建新的Word文档"工作流程

#### 编辑现有文档
- **您自己的文档 + 简单更改**
  使用"基本OOXML编辑"工作流程

- **他人的文档**
  使用**"Redlining工作流程"**（推荐默认）

- **法律、学术、商业或政府文档**
  使用**"Redlining工作流程"**（必需）

### 读取和分析内容

#### 文本提取
如果只需要读取文档的文本内容，应该使用pandoc将文档转换为markdown。Pandoc提供出色的文档结构保留支持，并可以显示跟踪更改：

```bash
# 转换文档为markdown，保留跟踪更改
pandoc --track-changes=all path-to-file.docx -o output.md
# 选项：--track-changes=accept/reject/all
```

#### 原始XML访问
需要原始XML访问用于：评论、复杂格式、文档结构、嵌入媒体和元数据。对于任何这些功能，您需要解包文档并读取其原始XML内容。

**解包文件**
```bash
python ooxml/scripts/unpack.py <office_file> <output_directory>
```

**关键文件结构**
- `word/document.xml` - 主要文档内容
- `word/comments.xml` - document.xml中引用的评论
- `word/media/` - 嵌入的图像和媒体文件
- 跟踪更改使用`<w:ins>`（插入）和`<w:del>`（删除）标签

### 创建新的Word文档

从零开始创建新的Word文档时，使用**docx-js**，它允许您使用JavaScript/TypeScript创建Word文档。

**工作流程**
1. **必须 - 读取整个文件**：完全从头到尾读取[`docx-js.md`](docx-js.md)（~500行）。**读取此文件时永远不要设置任何范围限制。**在继续创建文档之前，读取完整的文件内容以获取详细的语法、关键格式规则和最佳实践。

2. 使用Document、Paragraph、TextRun组件创建JavaScript/TypeScript文件（您可以假设所有依赖项都已安装，但如果没有，请参考下面的依赖项部分）

3. 使用Packer.toBuffer()导出为.docx

### 编辑现有的Word文档

编辑现有的Word文档时，使用**Document库**（一个用于OOXML操作的Python库）。该库自动处理基础设施设置并提供文档操作方法。对于复杂场景，您可以通过该库直接访问底层DOM。

**工作流程**
1. **必须 - 读取整个文件**：完全从头到尾读取[`ooxml.md`](ooxml.md)（~600行）。**读取此文件时永远不要设置任何范围限制。**读取完整的文件内容以获取Document库API和直接编辑文档文件的XML模式。

2. 解包文档：`python ooxml/scripts/unpack.py <office_file> <output_directory>`

3. 创建并运行使用Document库的Python脚本（参见ooxml.md中的"Document Library"部分）

4. 打包最终文档：`python ooxml/scripts/pack.py <input_directory> <office_file>`

Document库提供常见操作的高级方法和复杂场景的直接DOM访问。

### Redlining工作流程（文档审查）

此工作流程允许您在OOXML中实现之前使用markdown规划全面的跟踪更改。**关键**：对于完整的跟踪更改，您必须系统地实现所有更改。

**批处理策略**：将相关更改分组为3-10个更改的批次。这使得调试易于管理，同时保持效率。在移动到下一个之前测试每个批次。

**原则：最小化、精确的编辑**
实现跟踪更改时，只标记实际更改的文本。重复未更改的文本会使编辑更难审查，看起来不专业。将替换分解为：[未更改文本] + [删除] + [插入] + [未更改文本]。通过从原始中提取`<w:r>`元素并重用它来保留未更改文本的原始RSID。

示例 - 将句子中的"30 days"更改为"60 days"：
```python
# 不好 - 替换整个句子
'<w:del><w:r><w:delText>The term is 30 days.</w:delText></w:r></w:del><w:ins><w:r><w:t>The term is 60 days.</w:t></w:r></w:ins>'

# 好 - 只标记更改的内容，为未更改文本保留原始<w:r>
'<w:r w:rsidR="00AB12CD"><w:t>The term is </w:t></w:r><w:del><w:r><w:delText>30</w:delText></w:r></w:del><w:ins><w:r><w:t>60</w:t></w:r></w:ins><w:r w:rsidR="00AB12CD"><w:t> days.</w:t></w:r>'
```

#### 跟踪更改工作流程

1. **获取markdown表示**：转换文档为markdown，保留跟踪更改：
   ```bash
   pandoc --track-changes=all path-to-file.docx -o current.md
   ```

2. **识别和分组更改**：审查文档并识别所有需要的更改，将它们组织成逻辑批次：

   **定位方法**（用于在XML中查找更改）：
   - 章节/标题编号（例如，"Section 3.2"、"Article IV"）
   - 如果编号，段落标识符
   - 带有唯一周围文本的Grep模式
   - 文档结构（例如，"第一段"、"签名块"）
   - **不要使用markdown行号** - 它们不映射到XML结构

   **批处理组织**（每批分组3-10个相关更改）：
   - 按章节："批次1：第2节修订"、"批次2：第5节更新"
   - 按类型："批次1：日期更正"、"批次2：当事人名称更改"
   - 按复杂性：从简单的文本替换开始，然后处理复杂的结构更改
   - 顺序："批次1：第1-3页"、"批次2：第4-6页"

3. **阅读文档和解包**：
   - **必须 - 读取整个文件**：完全从头到尾读取[`ooxml.md`](ooxml.md)（~600行）。**读取此文件时永远不要设置任何范围限制。**特别注意"Document Library"和"Tracked Change Patterns"部分。
   - **解包文档**：`python ooxml/scripts/unpack.py <file.docx> <dir>`
   - **注意建议的RSID**：解包脚本将建议为您的跟踪更改使用的RSID。复制此RSID以在步骤4b中使用。

4. **分批实现更改**：逻辑地分组更改（按章节、按类型或按接近度）并在单个脚本中一起实现它们。这种方法：
   - 使调试更容易（更小的批次 = 更容易隔离错误）
   - 允许增量进度
   - 保持效率（3-10个更改的批次大小效果很好）

   **建议的批处理分组**：
   - 按文档章节（例如，"第3节更改"、"定义"、"终止条款"）
   - 按更改类型（例如，"日期更改"、"当事人名称更新"、"法律术语替换"）
   - 按接近度（例如，"第1-3页的更改"、"文档前半部分的更改"）

   对于每批相关更改：

   **a. 将文本映射到XML**：在`word/document.xml`中grep文本以验证文本如何跨`<w:r>`元素分割。

   **b. 创建并运行脚本**：使用`get_node`查找节点，实现更改，然后`doc.save()`。参见ooxml.md中的**"Document Library"**部分以获取模式。

   **注意**：总是在编写脚本之前立即grep `word/document.xml`以获取当前行号并验证文本内容。每次脚本运行后行号都会更改。

5. **打包文档**：所有批次完成后，将解包目录转换回.docx：
   ```bash
   python ooxml/scripts/pack.py unpacked reviewed-document.docx
   ```

6. **最终验证**：对完整文档进行全面检查：
   - 转换最终文档为markdown：
     ```bash
     pandoc --track-changes=all reviewed-document.docx -o verification.md
     ```
   - 验证所有更改都正确应用：
     ```bash
     grep "original phrase" verification.md  # 应该找不到
     grep "replacement phrase" verification.md  # 应该找到
     ```
   - 检查是否引入了任何意外更改

### 将文档转换为图像

要视觉分析Word文档，使用两步过程将它们转换为图像：

1. **将DOCX转换为PDF**：
   ```bash
   soffice --headless --convert-to pdf document.docx
   ```

2. **将PDF页面转换为JPEG图像**：
   ```bash
   pdftoppm -jpeg -r 150 document.pdf page
   ```
   这会创建`page-1.jpg`、`page-2.jpg`等文件。

选项：
- `-r 150`：将分辨率设置为150 DPI（调整质量/大小平衡）
- `-jpeg`：输出JPEG格式（如果首选，使用`-png`作为PNG）
- `-f N`：要转换的第一页（例如，`-f 2`从第2页开始）
- `-l N`：要转换的最后一页（例如，`-l 5`在第5页停止）
- `page`：输出文件的前缀

特定范围的示例：
```bash
pdftoppm -jpeg -r 150 -f 2 -l 5 document.pdf page  # 仅转换第2-5页
```

### 代码风格指南
**重要**：为DOCX操作生成代码时：
- 编写简洁的代码
- 避免冗长的变量名和冗余操作
- 避免不必要的print语句

### 依赖项

所需依赖项（如果不可用则安装）：

- **pandoc**：`sudo apt-get install pandoc`（用于文本提取）
- **docx**：`npm install -g docx`（用于创建新文档）
- **LibreOffice**：`sudo apt-get install libreoffice`（用于PDF转换）
- **Poppler**：`sudo apt-get install poppler-utils`（用于pdftoppm将PDF转换为图像）
- **defusedxml**：`pip install defusedxml`（用于安全XML解析）

### 常见使用场景

#### 场景1：创建新的合同文档
1. 使用docx-js创建新文档
2. 添加标题、段落和格式化文本
3. 导出为.docx文件

#### 场景2：编辑现有文档并添加跟踪更改
1. 使用pandoc将文档转换为markdown
2. 识别需要更改的部分
3. 解包文档
4. 使用Document库实现跟踪更改
5. 打包文档
6. 验证更改

#### 场景3：分析文档内容
1. 使用pandoc提取文本
2. 分析内容结构
3. 提取关键信息

#### 场景4：批量处理多个文档
1. 将相关更改分组为批次
2. 为每个批次创建脚本
3. 测试每个批次
4. 逐步实现所有更改

### 最佳实践

1. **对于专业文档**，始终使用Redlining工作流程
2. **批量处理时**，将更改分组为3-10个的批次
3. **实现跟踪更改时**，只标记实际更改的文本
4. **处理XML时**，注意`<w:r>`元素的结构
5. **验证更改**，使用pandoc转换和grep检查
6. **保持代码简洁**，避免冗余操作

### 故障排除

**问题**：文档格式丢失
- **解决方案**：使用Document库而不是直接XML编辑

**问题**：跟踪更改不显示
- **解决方案**：确保正确使用`<w:ins>`和`<w:del>`标签

**问题**：文本分割不正确
- **解决方案**：检查`<w:r>`元素结构，使用grep验证

**问题**：批处理后文档损坏
- **解决方案**：测试每个批次，逐步验证更改

---

## 总结

Awesome Claude Skills提供了丰富的工具集，涵盖文档处理、开发工具、商业营销、沟通写作、创意媒体、生产力组织等多个领域。每个技能都有其特定的用途和最佳实践，根据您的需求选择合适的技能可以大大提高工作效率。

DOCX技能特别适合处理专业的Word文档，支持创建、编辑、分析等全方位操作，特别是在处理需要跟踪更改的法律、学术、商业文档时非常有用。