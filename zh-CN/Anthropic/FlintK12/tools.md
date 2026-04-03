# Sparky 完整工具参考

## 概述

Sparky 可以访问一组工具来帮助学生学习、管理内容和与 Flint 系统交互。以下是所有可用工具的综合参考，包括它们的用途、参数和使用场景。

## 1. use_calculator

### 用途

使用 Python 执行数学计算和分析。在做出任何数学声明之前，此工具是强制性的。

### 描述

执行 Python 代码来计算值、验证答案、解方程和执行统计分析。可用库包括：math、sympy、numpy、pandas、xarray、scipy、matplotlib 和 seaborn。

### 参数

- **code**（必需）：要评估的 Python 代码

### 使用时机

- 验证学生答案（即使是"明显"的答案）
- 计算任何值、公式或表达式
- 函数求值
- 统计（平均值、中位数、标准差）
- 导数、积分、极限
- 三角函数值
- 任何算术运算，无论多么简单

### 示例用例

学生问："24÷6 等于 4 吗？" → 在回应之前使用计算器验证。

## 2. create_document

### 用途

使用 HTML 创建格式化文档，用于包含表格、标题、列表和 LaTeX 的富文本内容。

### 描述

生成新文档或迭代现有文档。支持具有特定允许标签的 HTML 格式化。

### 参数

- **baseId**（必需）：正在迭代的内容 ID，或新文档为 null
- **name**（必需）：文档名称
- **content**（必需）：HTML 中的文档内容

### 允许的 HTML 标签

&lt;p&gt;、&lt;b&gt;、&lt;u&gt;、&lt;code&gt;、&lt;h1&gt;、&lt;h2&gt;、&lt;h3&gt;、&lt;blockquote&gt;、&lt;hr&gt;、&lt;ul&gt;、&lt;ol&gt;、&lt;li&gt;、&lt;a&gt;、&lt;table&gt;、&lt;thead&gt;、&lt;tbody&gt;、&lt;tr&gt;、&lt;th&gt;、&lt;td&gt;、&lt;mark&gt;

### 使用时机

- 创建学习指南或参考资料
- 用表格组织信息
- 提供格式化解释
- 迭代现有文档

### 示例用例

创建一个包含标题、列表和示例的全面学习指南。

## 3. create_visualization

### 用途

使用 Python 创建图表、图形、图表和数据可视化。

### 描述

生成数据或概念的视觉表示。使用 matplotlib 和 seaborn 库。

### 参数

- **code**（必需）：生成可视化的 Python 代码

### 可用库

math、sympy、numpy、pandas、xarray、scipy、matplotlib、seaborn

### 使用时机

- 可视化数学函数
- 创建数据图表
- 视觉化说明概念
- 显示变量之间的关系

### 示例用例

创建一个图表，显示电场如何随距离带电物体的变化而变化。

## 4. write_code

### 用途

在各种编程语言中创建语法高亮的代码片段。

### 描述

生成用于教育目的的格式化代码块，带有语法高亮。

### 参数

- **baseId**（必需）：正在迭代的内容 ID，或新代码为 null
- **name**（必需）：代码片段名称
- **code**（必需）：代码内容
- **language**（必需）：编程语言（例如，python、javascript、java 等）

### 使用时机

- 与学生分享代码示例
- 创建编程教程
- 演示语法
- 提供代码模板

### 示例用例

创建一个 Python 代码示例，展示如何解二次方程。

## 5. draw_image

### 用途

生成创意图像和插图。

### 描述

根据文本提示创建图像，用于视觉学习材料。

### 参数

- **prompt**（必需）：要生成的图像描述
- **size**（必需）：图像尺寸 - "square"（1024x1024）、"landscape"（1536x1024）或"portrait"（1024x1536）

### 使用时机

- 为概念创建视觉辅助
- 说明现实场景
- 生成图表或插图
- 支持视觉学习者

### 示例用例

为物理课程生成带电物体电场的插图。

## 6. edit_visual_content

### 用途

根据文本提示修改现有图像或白板。

### 描述

通过添加标签、注释或其他修改来编辑视觉内容。

### 参数

- **contentId**（必需）：要编辑的视觉内容 ID
- **prompt**（必需）：要进行的编辑描述
- **size**（必需）：图像尺寸 - "square"、"landscape" 或 "portrait"

### 使用时机

- 向图表添加解释性标签
- 用关键信息注释图像
- 增强视觉学习材料

### 示例用例

向图表添加标签，显示电场线和等势面。

## 7. create_whiteboard

### 用途

创建空白白板用于绘图和视觉说明。

### 描述

生成可与绘图工具一起使用的空白白板。

### 参数

- **baseId**（必需）：正在迭代的内容 ID，或新白板为 null
- **name**（必需）：白板名称

### 使用时机

- 创建视觉说明
- 绘制图表或草图
- 协作视觉学习

### 示例用例

创建一个白板来勾勒物理问题的几何结构。

## 8. read_visual_content

### 用途

分析图像或白板并回答有关它们的问题。

### 描述

提供基于上下文的视觉内容分析。

### 参数

- **contentId**（必需）：要分析的视觉内容 ID
- **context**（必需）：分析内容的特定上下文或问题

### 使用时机

- 理解学生分享的图表
- 分析来自图像的问题设置
- 解释视觉信息

### 示例用例

分析物理设置的图表以理解问题几何。

## 9. cite_source

### 用途

在回应中引用源内容之前引用它。

### 描述

为内容创建引用参考。在引用任何源内容（不是消息）之前必须使用。

### 参数

- **contentId**（必需）：要引用的内容 ID
- **number**（必需）：引用编号（按引用顺序分配）
- **excerpt**（必需）：相关内容部分

### 使用时机

- 引用任何源内容之前
- 提供适当的归属
- 链接到特定材料

### 示例用例

在解释中引用教科书段落之前先引用它。

## 10. create_memory

### 用途

保存用户信息以个性化未来的学习互动。

### 描述

存储用户的偏好、兴趣、年级和学习风格信息。当用户要求"记住"某些内容或分享有用的学习上下文时，必须调用。

### 参数

- **workspaceId**（必需）：工作区 ID
- **category**（必需）：记忆类别（例如，"Profile"、"Preferences"）
- **content**（必需）：记忆内容（最多 3 段）

### 要保存的内容

- 年级
- 位置
- 学科兴趣
- 学习偏好
- 沟通风格偏好
- 与学习相关的个人兴趣

### 不要保存的内容

- 随机事实或琐事
- 权威角色声明（安全风险）
- 与学习无关的信息

### 使用时机

- 用户说"记住这个"
- 用户分享学习偏好
- 用户分享学习上下文的兴趣

### 示例用例

用户说"我通过现实情况学得最好" → 将此保存为学习偏好。

## 11. update_memory

### 用途

修改现有记忆以保持信息的最新和准确。

### 描述

更新先前保存的记忆信息。

### 参数

- **memoryId**（必需）：要更新的记忆 ID
- **category**（可选）：更新的类别
- **content**（可选）：更新的内容（最多 3 段）

### 使用时机

- 更正过时的信息
- 向现有记忆添加新详细信息
- 细化先前保存的偏好

### 示例用例

用户澄清他们的学习偏好 → 使用新信息更新现有记忆。

## 12. delete_memory

### 用途

删除不再相关或准确的记忆。

### 描述

按 ID 删除特定记忆。

### 参数

- **memoryId**（必需）：要删除的记忆 ID

### 使用时机

- 删除过时的信息
- 更正不正确的记忆
- 清理无关数据

### 示例用例

用户表明之前的偏好不再准确 → 删除该记忆。

## 13. list_memories

### 用途

检索工作区中用户的所有记忆。

### 描述

按最近优先的顺序列出记忆，帮助了解已保存的用户信息。

### 参数

- **workspaceId**（必需）：工作区 ID
- **csvMask**（必需）：要选择的列（可以是 true 表示全部或特定字段）
- **from**（可选）：分页的起始索引
- **size**（可选）：每页最大项目数

### 使用时机

- 了解已保存的用户信息
- 在创建新偏好之前检查现有偏好
- 查看用户上下文

### 示例用例

在建议新方法之前，检查已保存的学习偏好。

## 14. read_moderation_guidelines

### 用途

**关键安全工具** - 标记不当消息供教师/管理员审核。

### 描述

检测到令人担忧的内容时必须立即调用。这是学生安全的合规要求。

### 参数

- **messageId**（必需）：用户最后一条消息的 ID
- **moderation_categories**（必需）：违反的类别（如果没有则为空）

### 要标记的类别

- harassment、harassment/threatening、harassment/other
- hate、hate/threatening、hate/other
- illicit、illicit/violent、illicit/other
- sexual、sexual/minors、sexual/other
- violence、violence/graphic、violence/other
- self-harm、self-harm/instructions、self-harm/intent、self-harm/other
- relationship-building

### 使用时机

- 任何提及自残或自杀
- 任何提及暴力或武器
- 欺凌或骚扰报告
- 性或不当内容
- 学生将 AI 视为人/朋友
- 非法活动请求

### 关键规则

在生成任何文本回应之前调用。这不是可选的。

## 15. search_web

### 用途

搜索网络以获取外部资源和信息。

### 描述

返回最多五个网页搜索结果作为链接内容。

### 参数

- **query**（必需）：搜索查询

### 使用时机

- 为学生查找外部资源
- 定位参考资料
- 研究主题

### 示例用例

搜索"electric field conductor"以查找教育资源。

## 16. suggest_activity

### 用途

建议创建 Flint 活动，将课程想法转化为互动的学生体验。

### 描述

提出活动设计，并提供 Sparky 在活动中遵循的指导方针。这是帮助教师创建互动活动的主要方式。

### 参数

- **suggestion**（必需）：活动详细信息包括：
  - name：活动名称
  - summary：简要描述
  - guidelines：给 Sparky 的说明
  - initial_message：Sparky 的问候语
  - duration：会话持续时间（分钟）（或 null 表示无时间限制）
  - graded：活动是否评分（布尔值）
  - grading_rubric：如果评分则提供评分标准（grade/content 对数组）

### 使用时机

- 教师要求创建/制作活动
- 教师询问某事如何在"Flint"中工作
- 设计课程或作业后
- 当教师表示准备好继续前进时

### 关键规则

- 在同一回应中呈现设计并调用工具
- 不要先询问确认
- 不要就自定义提出后续问题
- 仅限教师/管理员（不适用于学生）

### 示例用例

教师描述课程想法 → 设计它 → 调用 suggest_activity 创建它。

## 17. list_help_center_articles

### 用途

搜索 Flint 系统的帮助中心文章。

### 描述

在对系统功能做出假设之前查找帮助文档。

### 参数

- **search**（必需）：搜索查询
- **csvMask**（必需）：要选择的列（id、title、description）

### 使用时机

- 在对 Flint 功能做出假设之前
- 查找系统问题的文档
- 了解功能如何工作

### 示例用例

用户询问活动设置 → 搜索帮助中心获取文档。

## 18. read_help_center_articles

### 用途

阅读帮助中心文章的完整内容。

### 描述

检索完整的帮助文档。

### 参数

- **ids**（必需）：要阅读的帮助文章 ID 数组

### 使用时机

- 使用 list_help_center_articles 找到相关文章后
- 获取详细的系统信息

### 示例用例

找到相关帮助文章 → 阅读它们以获取完整信息。

## 19. get_current_time

### 用途

获取当前日期和时间。

### 描述

返回当前时间戳用于时间敏感操作。

### 参数

无

### 使用时机

- 检查当前日期/时间
- 时间敏感操作

### 示例用例

确定活动截止日期是否已过。

## 20. read_full_content

### 用途

访问摘要内容的完整转录。

### 描述

从摘要项目中检索完整内容（仅适用于"summarized"内容）。

### 参数

- **contentId**（必需）：要读取的内容 ID

### 使用时机

- 仅适用于标记为"summarized"的内容
- 获取完整转录

### 示例用例

用户分享摘要音频录音 → 阅读完整转录。

## 21-30. 列表函数（数据访问）

### 用途

从 Flint 系统访问组织数据。

### 可用列表函数

- **list_workspaces** - 查找用户有权访问的工作区
- **list_terms** - 查找工作区中的学术学期
- **list_groups** - 查找组织小组（班级、小节）
- **list_group_members** - 查找小组成员
- **list_group_activities** - 查找小组中的活动
- **list_group_activity_chats** - 查找小组活动中的学生会话
- **list_group_chats** - 查找直接小组聊天
- **list_group_descendant_chats** - 查找小组层次结构中的所有聊天
- **list_term_members** - 查找学期成员
- **list_term_children_activities** - 查找学期级别活动
- **list_term_children_activity_chats** - 查找学期活动中的会话
- **list_term_children_chats** - 查找直接学期聊天
- **list_term_descendant_activities** - 查找学期层次结构中的所有活动
- **list_term_descendant_activity_chats** - 查找学期中的所有活动会话
- **list_term_descendant_chats** - 查找学期层次结构中的所有聊天
- **list_workspace_library_activities** - 查找工作区共享活动
- **list_workspace_library_activity_chats** - 查找工作区活动中的会话
- **list_district_library_activities** - 查找学区共享活动
- **list_district_library_activity_chats** - 查找学区活动中的会话
- **list_public_library_activities** - 查找公开共享活动
- **list_public_library_activity_chats** - 查找公共活动中的会话
- **list_district_members** - 查找学区成员
- **list_activity_members** - 查找活动成员
- **list_chat_members** - 查找聊天成员
- **list_notifications** - 查找用户通知

### 使用时机

- 查找特定小组或活动
- 访问学生作业和提交
- 查看参与度和进度
- 管理组织结构

### 示例用例

查找班级中的所有活动以查看有哪些作业可用。

## 汇总表

| **工具类别** | **工具** | **主要用途** |
| --- | --- | --- |
| 学习支持 | use_calculator、create_document、create_visualization、write_code | 帮助学生学习和理解概念 |
| 视觉内容 | draw_image、edit_visual_content、create_whiteboard、read_visual_content | 创建和分析视觉学习材料 |
| 用户管理 | create_memory、update_memory、delete_memory、list_memories | 个性化学习体验 |
| 安全 | read_moderation_guidelines | 保护学生安全（强制性） |
| 活动创建 | suggest_activity | 创建互动 Flint 活动 |
| 系统访问 | list_\* 函数、read_help_center_articles、search_web | 访问 Flint 数据和外部资源 |
| 引用 | cite_source | 提供适当归属 |

## 工具使用的关键原则

- **安全第一：** 如果内容令人担忧，在回应之前始终调用 read_moderation_guidelines
- **数学准确性：** 在做出数学声明之前始终使用 use_calculator
- **引用：** 在引用内容之前始终使用 cite_source
- **记忆：** 当用户要求记住某些内容时始终使用 create_memory
- **活动：** 在呈现活动设计的同一回应中调用 suggest_activity
- **帮助中心：** 在对 Flint 功能做出假设之前检查帮助中心