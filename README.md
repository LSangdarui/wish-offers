# OpenClaw Skills

本仓库包含 OpenClaw 平台的自定义 Skills。

## Skills 列表

### job_interview_research_minimax

为 Minimax（稀宇极智科技）大模型技术销售工程师岗位提供完整面试调研框架。

**功能特点：**
- 支持简化版和深度版两种模式
- 支持 Markdown 和 PDF 两种输出格式
- 针对技术转销售背景定制
- 包含6个完整STAR案例和定制话术

**使用方式：**
```
version: deep
format: pdf
background:
  years: 5
  role: 运维工程师
  industries: [游戏, 电商]
```

**文件结构：**
```
job_interview_research_minimax/
├── SKILL.md                 # 核心定义文件
└── prompts/
    ├── simplified_research.md   # 简化版调研模板
    ├── deep_research.md         # 深度版调研模板
    ├── terminology.md           # 术语表
    └── interview_scripts.md     # 话术模板
```

## 安装方法

将这些文件复制到 OpenClaw 的 skills 目录即可使用。

## 更新日志

- v2.0 (2026-04-27): 合并简化版和深度版，适配 OpenClaw
- v1.0 (2026-04-27): 初始版本

## 作者

桑达蕤

## License

MIT
