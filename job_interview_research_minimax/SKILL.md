---
name: job_interview_research_minimax
description: >-
  为 Minimax（稀宇极智科技）大模型技术销售工程师岗位提供完整面试调研框架。
  支持简化版和深度版两种模式，输出 Markdown 或 PDF 格式。
  适用于准备 AI 大模型/ToB 销售/技术销售类岗位面试。
metadata:
  version: "2.0"
  author: "桑达蕤"
  category: "面试准备"
  tags:
    - "面试调研"
    - "Minimax"
    - "技术销售"
    - "ToB销售"
    - "AI大模型"
  created_date: "2026-04-27"
  updated_date: "2026-04-27"
  requirements:
    - "WebSearch 工具（搜索公司和行业信息）"
    - "md_to_pdf.py 脚本（PDF转换）"
  input_params:
    - name: "version_type"
      type: "string"
      required: true
      description: "调研版本类型：simplified（简化版）或 deep（深度版）"
      enum: ["simplified", "deep"]
    - name: "output_format"
      type: "string"
      required: false
      default: "markdown"
      description: "输出格式：markdown 或 pdf"
      enum: ["markdown", "pdf"]
    - name: "user_background"
      type: "string"
      required: false
      description: "用户背景信息（用于深度版定制）"
  output_format:
    - "markdown"
    - "pdf"
  error_handling:
    - "当链接无法访问时明确报错，不随意发挥"
    - "数据缺失时标注来源受限，提供合理估算范围"
---

# Minimax 面试调研 Skill

## 用途

为准备 Minimax（稀宇极智科技）大模型技术销售工程师岗位的候选人提供系统化面试调研支持。

## 触发条件

当用户提到以下关键词时自动触发：
- "Minimax 面试"
- "稀宇科技 面试"
- "技术销售 面试准备"
- "大模型销售 调研"
- "Minimax 岗位"

## 使用流程

### 1. 选择版本类型

在使用本 Skill 前，系统会询问用户需要的版本：

| 版本 | 命令 | 内容 | 时长 |
|------|------|------|------|
| **简化版** | `version: simplified` | 核心信息速览 | 30分钟 |
| **深度版** | `version: deep` | 完整话术+定制案例 | 2-3小时 |

### 2. 选择输出格式

| 格式 | 命令 | 适用场景 |
|------|------|----------|
| **Markdown** | `format: markdown`（默认） | 电脑编辑、后续修改 |
| **PDF** | `format: pdf` | 打印、手机查看、分享 |

### 3. 提供背景信息（深度版需要）

如需深度定制，请提供：
```yaml
background:
  years_of_experience: "5年"
  current_role: "运维工程师"
  industry_experience: ["游戏", "电商"]
  cloud_experience: ["阿里云", "AWS"]
  ai_experience: true
  sales_experience: false
```

## 命令示例

### 简化版 + Markdown（默认）
```
帮我准备 Minimax 技术销售的面试调研
```

### 深度版 + PDF
```
我要深度版 Minimax 面试调研，输出 PDF。
背景：5年运维，在电商公司，有阿里云经验，想转销售。
```

### 完整参数
```
version: deep
format: pdf
background:
  years: 5
  role: SRE运维
  industries: [游戏, 电商]
  cloud: [阿里云]
  transition_to: 技术销售
```

## 数据来源与可靠性

### 可靠来源 ★★★★★
- 港交所招股书（官方披露）
- 2025年度财报（官方披露）
- MiniMax News 技术博客（官方）
- 阿里云/火山引擎客户案例（合作伙伴）
- 36氪、虎嗅等权威科技媒体

### 时效性
- 财务数据：2025年度（2026年3月发布）
- 产品信息：截至2026年4月
- 市场数据：2024-2025年行业报告

### 数据缺失处理
当信息无法获取时，系统将：
1. ⚠️ 明确标注"信息来源受限"
2. 📊 提供行业合理估算范围
3. 💡 建议在面试中直接询问

## 输出文件结构

```
输出/
├── Minimax面试调研报告.md      # 主报告（Markdown）
├── Minimax面试调研报告.pdf      # 打印版（PDF）
└── 附件/
    ├── 术语表.md                 # 专业术语解释
    ├── 话术模板.md               # 面试回答话术
    └── STAR案例集.md             # 深度版专属
```

## Prompt 模板

### 简化版 Prompt
加载 `prompts/simplified_research.md`

### 深度版 Prompt  
加载 `prompts/deep_research.md`

### 术语表
加载 `prompts/terminology.md`

### 话术模板
加载 `prompts/interview_scripts.md`

## 错误处理

### 链接无法访问
```
⚠️ 数据获取限制

以下信息无法从公开渠道获取：
- 具体原因：[链接失效/需要登录/反爬虫限制/内容变更]
- 影响范围：[财务数据/组织架构/具体薪酬]

替代方案：
- 使用 [备用数据来源]
- 或建议在面试中直接询问
```

### 信息不完整
```
⚠️ 信息不完整警告

当前调研基于有限信息，以下内容可能不完整：
- [列出缺失内容]

建议：
1. 在面试中验证关键数据
2. 通过脉脉/看准网了解内部信息
3. 通过人脉获取一手资料
```

## 版本历史

| 版本 | 日期 | 更新内容 |
|------|------|----------|
| 2.0 | 2026-04-27 | 合并简化版和深度版，适配 OpenClaw |
| 1.0 | 2026-04-27 | 初始版本，分为两个独立 Skill |

## 参考资源

- GitHub 仓库：https://github.com/LSangdarui/wish-offers
- 详细术语：[prompts/terminology.md](prompts/terminology.md)
- 面试话术：[prompts/interview_scripts.md](prompts/interview_scripts.md)

---

*Skill版本：v2.0（OpenClaw适配版）*  
*更新日期：2026-04-27*  
*适配平台：OpenClaw / Cursor*
