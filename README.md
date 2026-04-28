# Wish Offers — 通用面试调研 Skill

> 输入任何「公司 + 岗位」，自动生成完整的面试准备包。
> 不限行业，不限公司，不限岗位类型。

---

## 这个 Skill 能做什么

把面试前的"信息搜集 + 自我定位 + 话术准备"全流程自动化。

### 简化版（30 分钟出报告）

适合：投了简历但还没收到面试通知，想快速了解一下 / 海投阶段批量预热

输出：
- 公司概况（融资、营收、战略）
- 核心产品与差异化
- 市场与竞品分析
- 岗位职责与薪酬
- 高频问题回答 + 反向提问
- 行业术语速查表

### 深度版（2-3 小时全面准备）

适合：拿到了重要面试，需要逐个问题准备 / 转行 / 跳槽到目标公司

输出（基于你的真实背景）：
- 三大核心优势提炼
- 岗位匹配度逐项打分
- 6 个完整 STAR 案例（基于你的项目）
- 8-10 个核心问题的定制话术
- 30 秒 + 1 分钟两版电梯演讲
- 16 个反向提问清单
- 面试前 3 天准备清单

---

## 快速开始

### 安装

```bash
# 克隆到你的 skills 目录
git clone https://github.com/LSangdarui/wish-offers.git ~/.agents/skills/wish-offers

# 或者下载 ZIP 后手动放到 skills 目录
```

> OpenClaw / Cursor 等 Agent 平台的 skills 目录路径可能略有不同，常见的是：
> - `~/.agents/skills/`
> - `~/.openclaw/skills/`
> - `~/.cursor/skills/`

### 使用

#### 交互方式：问答收集，确认后执行

Skill 被触发后，会用**问答方式**逐步收集信息，不会默认直接开始分析。

整个流程分 6 步提问，每次只问一个问题，等你回答后才继续：

```
第 1 问：你要准备哪家公司的面试？
↓（你回答：字节跳动 或 https://xxx）

第 2 问：你应聘的岗位是？
↓（你回答：后端工程师）

第 3 问：JD 能给我看一下吗？
↓（你粘贴 JD 文字 或 发 JD 链接）

第 4 问：简化版还是深度版？
  - 简化版：30 分钟出报告，适合快速预热
  - 深度版：完整准备包，需要你的背景信息
↓（你回答：简化版 / 深度版）

第 5 问：
  简化版 → 有没有想附上的背景（可选）
  深度版 → 简历 PDF 路径 或 文字背景（建议提供）
↓（你回答）

第 6 问：Markdown 还是 PDF 输出？
↓（你回答）

→ Skill 复述一遍你的信息，你确认 → 开始调研
```

#### 支持的输入形式

| 问题 | 支持的形式 |
|------|-----------|
| 公司 | 公司名 **或** 公司官网/招聘页 URL |
| 岗位 | 文字 |
| JD | JD 全文 **或** JD 链接 |
| 背景 | 文字 / PDF 简历路径 / Markdown 文件路径 |
| 项目 | 文字 **或** GitHub / Demo URL |

#### 如果你想一次性提供所有信息

Skill 会识别你已经提供的部分，只补问缺失的字段（但**输出格式必须单独确认**，不会默认）。

示例：
```
帮我准备面试

公司：Minimax
岗位：大模型技术销售
JD：https://www.minimaxi.com/careers/xxx
简历：~/Documents/简历.pdf
```

Skill 会说："好，公司、岗位、JD 和简历都有了——你要简化版还是深度版？"

---

## 文件结构

```
wish-offers/
├── SKILL.md                          # Skill 元数据 + 调用入口
├── README.md                         # 本文件
└── prompts/
    ├── simplified_research.md        # 简化版调研框架
    ├── deep_research.md              # 深度版调研框架
    ├── interview_scripts.md          # 通用面试话术与反向提问
    └── terminology.md                # 行业术语库（10 个行业）
```

---

## 输入参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|-----|------|
| `company` | string \| URL | ✅ | 公司名 或 公司官网/招聘页链接 |
| `position` | string | ✅ | 岗位简称（如：技术销售） |
| `jd_content` | string \| URL | ✅ | JD 文字 或 JD 链接 |
| `version_type` | string | ❌ | `simplified`（默认）/ `deep` |
| `user_background` | string \| PDF \| MD | ❌（深度版强烈建议） | 文字描述 / PDF 简历 / Markdown 简历 |
| `key_projects` | string \| URL[] | ❌ | 文字描述 或 GitHub/Demo 链接列表 |
| `output_format` | string | ❌ | `markdown`（默认）/ `pdf` |

### 三种必填输入的支持形式

| 字段 | 支持形式 | Skill 处理方式 |
|------|---------|---------------|
| 公司 | 公司名 | 直接 WebSearch |
| 公司 | 公司 URL | WebFetch 抓取 + 补充 WebSearch |
| 岗位 | 文字 | 直接使用 |
| JD | JD 文字 | 直接结构化提取 |
| JD | JD URL | WebFetch 抓取后再提取 |

### 选填的多种格式

| 字段 | 文字 | PDF | Markdown | URL | Word |
|------|:---:|:---:|:--------:|:---:|:----:|
| user_background | ✅ | ✅ | ✅ | ❌ | ⚠️ 需先转换 |
| key_projects | ✅ | ❌ | ✅ | ✅ | ❌ |

### 深度版的 background 内容建议（无论用哪种形式都建议覆盖）

```yaml
建议涵盖的核心信息:
  - years_of_experience: "5 年"
  - current_role: "运维工程师"
  - industries_worked: ["游戏", "电商"]
  - key_projects: 至少 2 个有量化数据的项目
  - core_skills: ["K8s", "Python", "阿里云"]
  - transition_motivation: "想转技术销售"

加分项（有则提供）:
  - customer_resources: "游戏行业 40+ 联系人"
  - unique_advantage: "经手 1.5 亿+ 采购"
  - ai_experience: "GPT/Claude 应用经验"
```

> 如果你提供的是 PDF 简历，以上信息会从简历自动提取，不必再额外重复。

---

## 支持的行业（已配置术语库）

- AI / 大模型
- 云计算 / IaaS
- SaaS / B 端软件
- 互联网消费 / C 端
- 电商 / 跨境
- 金融 / 支付 / Fintech
- 游戏 / 娱乐
- 硬件 / 半导体
- 自动驾驶 / 出行
- 销售 / 商业通用（任何 ToB 销售岗）

如果你的目标公司不在这些行业里，Skill 会用通用框架处理，并在调研中自动学习该行业的术语。

---

## 数据来源与可靠性

### 推荐来源（按可靠性排序）

| 来源 | 可靠性 | 适合调研的内容 |
|------|--------|---------------|
| 官网 / 招股书 / 财报 | ★★★★★ | 财务、战略、产品 |
| 官方技术博客 | ★★★★★ | 技术细节、产品更新 |
| 36氪 / 虎嗅 / 财新 / Bloomberg | ★★★★☆ | 行业分析、商业动态 |
| LinkedIn / 脉脉 | ★★★☆☆ | 团队规模、内部文化 |
| 看准网 / Glassdoor | ★★★☆☆ | 薪资、面试体验 |
| 知乎 / 小红书 | ★★☆☆☆ | 主观评价、补充视角 |

### 信息缺失时的处理

Skill 会主动标注：

```
⚠️ 数据获取限制
[具体信息] 无法从公开渠道获取，原因：[xxx]

替代方案：
- 使用 [备用来源]
- 基于行业均值估算（已标注）
- 建议在面试中直接询问
```

---

## 输出示例

### 简化版报告目录

```
# {公司} 面试调研报告（简化版）
├── 一、公司概况
│   ├── 1.1 基本信息
│   ├── 1.2 融资历程
│   ├── 1.3 财务健康度
│   └── 1.4 战略方向
├── 二、核心业务与产品
├── 三、市场与竞品分析
├── 四、岗位深度分析
├── 五、面试准备清单
└── 六、行业术语速查表
```

### 深度版报告目录

```
# {公司} 面试调研报告（深度版）
├── 一、个人定位分析
│   ├── 三大核心优势
│   ├── 岗位匹配度评估
│   └── 短板弥补策略
├── 二、6 个 STAR 案例
├── 三、定制回答话术（8-10 问）
├── 四、电梯演讲模板（30 秒 + 1 分钟）
├── 五、反向提问清单（16 个）
├── 六、面试前 3 天准备计划
└── 附件：术语表 / 公司分析 / 竞品对比
```

---

## 更新

```bash
cd ~/.agents/skills/wish-offers
git pull origin main
```

---

## 故障排除

### Skill 无法加载

1. 检查目录路径是否正确（如 `~/.agents/skills/wish-offers/SKILL.md` 必须存在）
2. 检查 `SKILL.md` 顶部的 metadata（`name`、`description` 是否完整）
3. 重启你的 Agent 客户端

### PDF 转换失败

```bash
# Python 依赖
pip install markdown weasyprint

# macOS 额外依赖
brew install pango gdk-pixbuf libffi

# Ubuntu/Debian
sudo apt-get install libpango1.0-dev
```

或者使用替代方案：
- VS Code 插件 `Markdown PDF`
- 在线工具：https://www.markdowntopdf.com/

### 公司搜索不到

可能原因：
- 创业初期的小公司
- 公司名拼写需要确认
- 信息保密度较高（如军工类）

建议补充：
- 公司官网链接
- 内部员工 / 猎头提供的一手信息
- 让 Skill 用行业标准给出通用框架

---

## 更新日志

| 版本 | 日期 | 更新内容 |
|------|------|---------|
| v3.2 | 2026-04-28 | **调研纪律模块**：强制溯源（每条数据附来源 URL）；双源交叉验证关键数据；禁止推断填写，无法获取必须显式报告；**STAR 反幻觉规则**：案例数字 100% 基于用户简历，禁止捏造；匹配度评分必须附具体证据 |
| v3.1 | 2026-04-27 | **必填项支持链接形式**（公司 URL、JD URL）；**新增 JD 必填字段**；**选填项支持 PDF 简历**（自动 Read 解析）；**项目支持 GitHub/Demo 链接**；新增「输入解析」阶段，所有输入源走统一处理流程 |
| v3.0 | 2026-04-27 | 改造为通用版，支持任何公司、任何岗位；新增 10 个行业术语库；优化深度版 STAR 模板和定制话术 |
| v2.0 | 2026-04-27 | 合并简化版与深度版，适配 OpenClaw 元数据规范 |
| v1.0 | 2026-04-27 | 初始版本（仅 Minimax 特化） |

---

## 许可

- **License**：MIT

---

## 相关链接

- 仓库：https://github.com/LSangdarui/wish-offers
- 反馈：https://github.com/LSangdarui/wish-offers/issues
- 配套 Skill：[tob-sales-assistant](https://github.com/LSangdarui/tob-sales-assistant)（ToB 销售助手）

---

**最后更新**：2026-04-28
