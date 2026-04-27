# OpenClaw Skills

本仓库包含 OpenClaw 平台的自定义 Skills。

## 📋 Skills 列表

### job_interview_research_minimax

为 Minimax（稀宇极智科技）大模型技术销售工程师岗位提供完整面试调研框架。

**功能特点：**
- 支持简化版和深度版两种模式
- 支持 Markdown 和 PDF 两种输出格式
- 针对技术转销售背景定制
- 包含6个完整STAR案例和定制话术

**文件结构：**
```
job_interview_research_minimax/
├── SKILL.md                 # 核心定义文件（含 metadata 配置）
└── prompts/
    ├── simplified_research.md   # 简化版调研模板
    ├── deep_research.md         # 深度版调研模板
    ├── terminology.md           # 术语表
    └── interview_scripts.md     # 话术模板
```

---

## 🚀 安装方法

### 方法一：直接复制到 OpenClaw skills 目录（推荐）

#### 步骤 1：找到 OpenClaw skills 目录

OpenClaw 的 skills 目录通常位于：

| 平台 | 默认路径 |
|------|----------|
| **macOS** | `~/.openclaw/skills/` |
| **Linux** | `~/.openclaw/skills/` |
| **Windows** | `%USERPROFILE%\.openclaw\skills\` |

如果没有该目录，手动创建：
```bash
mkdir -p ~/.openclaw/skills
```

#### 步骤 2：克隆本仓库

```bash
# 进入 OpenClaw skills 目录
cd ~/.openclaw/skills

# 克隆本仓库
git clone https://github.com/LSangdarui/wish-offers.git job_interview_research_minimax

# 或者使用 SSH（如果你已配置 SSH key）
git clone git@github.com:LSangdarui/wish-offers.git job_interview_research_minimax
```

#### 步骤 3：验证安装

安装完成后，目录结构应该是：
```
~/.openclaw/skills/
└── job_interview_research_minimax/
    ├── SKILL.md
    ├── README.md
    └── prompts/
        ├── simplified_research.md
        ├── deep_research.md
        ├── terminology.md
        └── interview_scripts.md
```

#### 步骤 4：重启 OpenClaw

安装完成后，重启 OpenClaw 客户端，Skill 会自动加载。

---

### 方法二：手动下载安装

如果不方便使用 git，可以手动下载安装：

#### 步骤 1：下载文件

1. 访问 https://github.com/LSangdarui/wish-offers
2. 点击 "Code" → "Download ZIP"
3. 解压 ZIP 文件

#### 步骤 2：复制到 skills 目录

```bash
# 创建 skills 目录（如果不存在）
mkdir -p ~/.openclaw/skills

# 复制解压后的文件夹
mv ~/Downloads/wish-offers-main ~/.openclaw/skills/job_interview_research_minimax
```

---

### 方法三：在 Cursor 中使用（作为 Cursor Skill）

本 Skill 也兼容 Cursor 的 Skill 系统。

#### 安装步骤：

```bash
# 进入 Cursor skills 目录
cd ~/.cursor/skills

# 克隆本仓库
git clone https://github.com/LSangdarui/wish-offers.git job-interview-research-minimax

# 或者创建软链接（如果你已经在 OpenClaw 中安装）
ln -s ~/.openclaw/skills/job_interview_research_minimax ~/.cursor/skills/job-interview-research-minimax
```

---

## 📖 使用方法

### 基本用法

安装完成后，在 OpenClaw 中输入以下指令即可使用：

```
帮我准备 Minimax 大模型技术销售工程师的面试调研
```

OpenClaw 会自动识别并加载本 Skill，然后询问你需要哪个版本和格式。

### 指定版本和格式

#### 简化版 + Markdown（默认）
```
version: simplified
format: markdown
```

#### 深度版 + PDF
```
version: deep
format: pdf
background:
  years: 5
  role: 运维工程师
  industries: [游戏, 电商]
```

### 完整示例

```
我需要深度版的 Minimax 面试调研报告，输出为 PDF。

我的背景：
- 工作年限：5年
- 当前岗位：SRE运维工程师
- 公司背景：电商公司
- 项目经验：千万级上云项目、年度降本800万
- 技能特长：K8s、Python、阿里云
- 转型方向：技术销售
```

---

## ⚙️ 配置说明

### 输入参数（Input Params）

| 参数名 | 类型 | 必填 | 默认值 | 说明 |
|--------|------|------|--------|------|
| `version_type` | string | 是 | - | 调研版本：`simplified`（简化版）或 `deep`（深度版） |
| `output_format` | string | 否 | `markdown` | 输出格式：`markdown` 或 `pdf` |
| `user_background` | string | 否 | - | 用户背景信息（用于深度版定制） |

### 版本对比

| 版本 | 适用场景 | 内容量 | 时长 |
|------|----------|--------|------|
| **简化版** | 快速了解公司 | ~5,000字 | 30分钟 |
| **深度版** | 深度面试准备 | ~20,000字 | 2-3小时 |

### 输出格式对比

| 格式 | 适用场景 | 特点 |
|------|----------|------|
| **Markdown** | 电脑编辑、后续修改 | 可编辑、易管理 |
| **PDF** | 打印、手机查看、分享 | 排版美观、便携 |

---

## 📊 数据来源与可靠性

### 可靠数据来源 ★★★★★
- Minimax 招股书（港交所公开信息）
- 2025年度财报（官方披露）
- MiniMax News 技术博客（官方）
- 阿里云/火山引擎客户案例（合作伙伴）
- 36氪、虎嗅等权威科技媒体报道

### 数据时效性
- 财务数据：2025年度（2026年3月发布）
- 产品信息：截至2026年4月
- 市场数据：2024-2025年行业报告

### 数据缺失处理
当某些信息无法从公开渠道获取时，Skill 会：
1. ⚠️ 明确标注"信息来源受限，以下为行业推测"
2. 📊 提供基于行业平均水平的合理估算范围
3. 💡 建议在面试中直接询问验证

---

## 🔄 更新方法

当本仓库有更新时，可以通过以下方式更新：

### 方法一：Git 拉取更新（推荐）

```bash
cd ~/.openclaw/skills/job_interview_research_minimax
git pull origin main
```

### 方法二：重新克隆

```bash
# 删除旧版本
rm -rf ~/.openclaw/skills/job_interview_research_minimax

# 重新克隆
cd ~/.openclaw/skills
git clone https://github.com/LSangdarui/wish-offers.git job_interview_research_minimax
```

---

## 🐛 故障排除

### 问题 1：Skill 无法加载

**症状**：输入指令后没有识别到 Skill

**解决方案**：
1. 检查目录结构是否正确
2. 确保 SKILL.md 文件存在且格式正确
3. 重启 OpenClaw 客户端
4. 检查 OpenClaw 日志（通常在 `~/.openclaw/logs/`）

### 问题 2：GitHub 连接失败

**症状**：无法克隆仓库

**解决方案**：
```bash
# 检查 SSH key
ls -la ~/.ssh/id_*

# 如果没有 SSH key，生成一个
ssh-keygen -t ed25519 -C "your_email@example.com"

# 将公钥添加到 GitHub
cat ~/.ssh/id_ed25519.pub
# 复制输出内容到 GitHub Settings -> SSH and GPG keys -> New SSH key

# 测试连接
ssh -T git@github.com
```

### 问题 3：缺少依赖工具

**症状**：PDF 转换失败

**解决方案**：
```bash
# 安装 Python 依赖
pip install markdown weasyprint

# macOS 额外依赖
brew install pango gdk-pixbuf libffi

# Ubuntu/Debian 额外依赖
sudo apt-get install libpango1.0-dev
```

---

## 📝 更新日志

| 版本 | 日期 | 更新内容 |
|------|------|----------|
| v2.0 | 2026-04-27 | 合并简化版和深度版，适配 OpenClaw 格式规范，添加 metadata 配置 |
| v1.0 | 2026-04-27 | 初始版本，分为两个独立 Skill |

---

## 👤 作者信息

- **作者**：桑达蕤
- **邮箱**：18374722586@163.com
- **GitHub**：https://github.com/LSangdarui

---

## 📄 License

MIT License

---

## 🤝 贡献指南

如果你对本 Skill 有改进建议或发现了问题，欢迎：
1. 提交 Issue：https://github.com/LSangdarui/wish-offers/issues
2. 提交 Pull Request
3. 联系作者

---

## 🔗 相关链接

- **本仓库**：https://github.com/LSangdarui/wish-offers
- **Minimax 官网**：https://www.minimaxi.com
- **Minimax 开放平台**：https://api.minimaxi.com
- **OpenClaw 文档**：[待添加]

---

**最后更新**：2026-04-27
