# 行业术语速查表（通用版）

> 本文件是按行业分类的术语库，用于在调研报告中插入「术语速查表」。
> 实际使用时，根据目标公司所在行业，挑选 15-25 个最相关的术语放入报告。
> 如果目标公司涉及多个行业（如字节跳动），按主营业务挑选。

---

## 使用指南

### 第一步：识别公司所在行业

参考以下行业标签：

| 行业标签 | 对应板块 | 典型公司示例 |
|---------|---------|------------|
| AI / 大模型 | AI 大模型相关 | OpenAI、Anthropic、Minimax、智谱、DeepSeek |
| 云计算 / IaaS | 云计算相关 | 阿里云、AWS、火山引擎、腾讯云 |
| SaaS / B 端软件 | SaaS / 企业服务 | Salesforce、Zoom、飞书、钉钉 |
| 互联网消费 / C 端 | 互联网产品 | 字节跳动、美团、小红书、拼多多 |
| 电商 / 跨境 | 电商相关 | SHEIN、亚马逊、京东、Temu |
| 金融 / 支付 / Fintech | 金融科技 | 蚂蚁、Stripe、招行、平安科技 |
| 游戏 / 娱乐 | 游戏行业 | 米哈游、腾讯游戏、网易、Epic |
| 硬件 / 半导体 | 硬件相关 | 苹果、华为、英伟达、联想 |
| 自动驾驶 / 出行 | 出行/AD | 滴滴、Uber、Tesla、小马智行 |
| 销售 / 商业通用 | 跨行业通用 | 任何 ToB 销售岗位 |

### 第二步：挑选 15-25 个术语

按以下原则挑选：
- 一定包含的：通用商业术语（5-8 个）
- 必须包含的：该行业的核心术语（8-12 个）
- 加分项：该公司特有的术语 / 黑话（2-5 个，需自行补充）

---

## 一、AI / 大模型行业术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **AGI** | Artificial General Intelligence | 通用人工智能，像人一样什么都能干的 AI |
| **LLM** | Large Language Model | 大语言模型，如 ChatGPT、Claude、Minimax-M2 |
| **MaaS** | Model as a Service | 模型即服务，按 API 调用付费 |
| **MoE** | Mixture of Experts | 混合专家模型，按需激活部分参数 |
| **Token** | 模型最小处理单元 | 1 汉字≈1-2 token，1 英文单词≈1.3 token |
| **多模态** | Multi-modal | 同时处理文本+语音+图片+视频 |
| **长上下文** | Long Context | 模型能记住的输入长度（如 100 万 token） |
| **推理** | Inference | 模型生成答案的过程 |
| **训练** | Training | 用数据让模型学习的过程 |
| **微调** | Fine-tuning | 在通用模型基础上用专业数据再训练 |
| **RAG** | Retrieval-Augmented Generation | 检索增强生成，先查后答 |
| **Agent** | 智能体 | 能自主规划、调用工具的 AI 系统 |
| **POC** | Proof of Concept | 概念验证，给客户做试用 Demo |
| **Prompt Engineering** | 提示工程 | 设计指令让模型输出更好的结果 |
| **幻觉** | Hallucination | 模型编造看似合理但错误的内容 |
| **API** | Application Programming Interface | 系统间互通的接口 |
| **SLA** | Service Level Agreement | 服务等级协议，承诺可用性 |
| **TPS / QPS** | Transactions/Queries Per Second | 每秒事务/查询数，衡量并发性能 |
| **首 Token 延迟** | TTFT (Time to First Token) | 从输入到第一个字输出的时间 |
| **Tokenizer** | 分词器 | 把文字切成模型能理解的小块 |

---

## 二、云计算 / IaaS 行业术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **IaaS** | Infrastructure as a Service | 基础设施即服务，租服务器/网络/存储 |
| **PaaS** | Platform as a Service | 平台即服务，租开发环境 |
| **SaaS** | Software as a Service | 软件即服务，直接用云上的软件 |
| **K8s** | Kubernetes | 容器编排，管理大量容器 |
| **Docker** | 容器化平台 | 把应用打包成"集装箱"运行 |
| **微服务** | Microservices | 把大系统拆成多个小服务 |
| **Serverless** | 无服务器 | 不管服务器，按调用计费 |
| **CDN** | Content Delivery Network | 内容分发网络，让内容更快到用户 |
| **VPC** | Virtual Private Cloud | 虚拟私有云，逻辑隔离的网络 |
| **EBS / OSS** | Elastic Block Store / Object Storage Service | 块存储 / 对象存储 |
| **DBaaS** | Database as a Service | 数据库即服务 |
| **FinOps** | Financial Operations | 云成本财务化运营 |
| **TCO** | Total Cost of Ownership | 总拥有成本（购买+运维+迁移） |
| **混合云** | Hybrid Cloud | 公有云+私有云的组合 |
| **多云** | Multi-cloud | 同时用多个云厂商的服务 |
| **边缘计算** | Edge Computing | 把计算下沉到离用户近的地方 |
| **可用性区** | AZ (Availability Zone) | 同地区内物理隔离的数据中心 |
| **灾备** | Disaster Recovery | 灾难发生时的备份恢复方案 |
| **SLO / SLI** | Service Level Objective / Indicator | 服务等级目标 / 指标 |
| **AIOps** | AI for IT Operations | AI 驱动的智能运维 |

---

## 三、SaaS / B 端软件术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **MRR / ARR** | Monthly / Annual Recurring Revenue | 月度/年度经常性收入 |
| **NDR / NRR** | Net Dollar Retention | 净收入留存率（包含续费+扩展+流失） |
| **GDR** | Gross Dollar Retention | 毛收入留存（不含扩展） |
| **CAC** | Customer Acquisition Cost | 客户获取成本 |
| **LTV** | Lifetime Value | 客户生命周期价值 |
| **LTV/CAC** | LTV 与 CAC 比值 | 健康 SaaS > 3 |
| **Payback Period** | 回本周期 | 客户付的钱多久能覆盖 CAC |
| **Churn Rate** | 流失率 | 客户/收入流失的比例 |
| **DAU / MAU** | Daily / Monthly Active Users | 日 / 月活跃用户 |
| **Stickiness** | 粘性 | DAU/MAU 比值 |
| **Onboarding** | 用户引导 | 新客户上手过程 |
| **Activation** | 激活 | 用户完成关键动作（如发第一条消息） |
| **Time to Value** | 价值实现时间 | 用户从注册到感受到价值的时间 |
| **PLG** | Product-Led Growth | 产品驱动增长（不靠销售推） |
| **SLG** | Sales-Led Growth | 销售驱动增长 |
| **Self-Serve** | 自助式 | 用户自己注册、配置、付费 |
| **Tier / 套餐** | Tier / Pricing Plan | 价格分层 |
| **Seats / 席位** | Per-Seat Pricing | 按用户数收费 |
| **Usage-Based** | 按使用量计费 | 用多少付多少 |
| **POC** | Proof of Concept | 概念验证 |

---

## 四、互联网消费 / C 端术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **GMV** | Gross Merchandise Volume | 商品交易总额（不等于收入） |
| **DAU / MAU** | Daily / Monthly Active Users | 日 / 月活跃用户 |
| **ARPU** | Average Revenue Per User | 单用户平均收入 |
| **ARPPU** | Average Revenue Per Paying User | 单付费用户平均收入 |
| **留存率** | Retention Rate | 次留 / 7 留 / 30 留 |
| **CAC** | Customer Acquisition Cost | 获客成本 |
| **ROI** | Return on Investment | 投资回报率 |
| **LTV** | Lifetime Value | 用户生命周期价值 |
| **AB Test** | A/B Testing | 对照实验 |
| **PMF** | Product-Market Fit | 产品-市场契合 |
| **冷启动** | Cold Start | 0 到 1 阶段的获客 / 内容 |
| **私域** | Private Traffic | 自己掌握的用户流量（如微信群） |
| **公域** | Public Traffic | 平台分发的流量 |
| **种子用户** | Seed Users | 早期最匹配的核心用户 |
| **裂变** | Viral Growth | 老带新的传播机制 |
| **漏斗** | Funnel | 用户转化路径（曝光 → 点击 → 转化） |
| **GMV 转化率** | GMV Conversion Rate | 流量到 GMV 的比例 |
| **复购率** | Repurchase Rate | 用户重复购买的比例 |
| **CTR** | Click-Through Rate | 点击率 |
| **CVR** | Conversion Rate | 转化率 |

---

## 五、电商 / 跨境术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **GMV** | Gross Merchandise Volume | 商品交易总额 |
| **客单价** | Average Order Value | 单笔订单平均金额 |
| **退货率** | Return Rate | 退货占总订单的比例 |
| **库存周转率** | Inventory Turnover | 一年库存被卖几次 |
| **SKU** | Stock Keeping Unit | 最小库存单位 |
| **SPU** | Standard Product Unit | 标准产品单元（一个 SPU 可有多个 SKU） |
| **DTC** | Direct to Consumer | 品牌直接面向消费者，不通过中间商 |
| **白牌 / 贴牌** | Private Label / OEM | 没有强品牌的产品 / 代工产品 |
| **小单快返** | Small Batch Quick Reorder | 先小批量测试再快速补货 |
| **柔性供应链** | Flexible Supply Chain | 可快速应变的供应链体系 |
| **跨境电商** | Cross-Border E-commerce | 跨国销售 |
| **海外仓** | Overseas Warehouse | 在海外建立的仓储 |
| **FBA** | Fulfillment by Amazon | 亚马逊代发模式 |
| **半托管 / 全托管** | Semi/Full Managed | 平台管理供应链的程度 |
| **ASIN** | Amazon Standard ID Number | 亚马逊产品 ID |
| **UV / PV** | Unique / Page Views | 独立访客数 / 页面浏览量 |
| **CR / CVR** | Conversion Rate | 转化率 |
| **CPC / CPM** | Cost Per Click / Mille | 单次点击/千次曝光成本 |

---

## 六、金融 / 支付 / Fintech 术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **TPV** | Total Payment Volume | 总支付交易额 |
| **Take Rate** | 平台抽佣率 | 平台从交易中抽取的比例 |
| **MDR** | Merchant Discount Rate | 商户费率（卡组织+清算+发卡的总费率） |
| **GMV / TPV** | Gross / Total Volume | 交易总额 |
| **ACH** | Automated Clearing House | 美国自动清算系统（类似国内网联） |
| **POS** | Point of Sale | 销售终端 |
| **KYC** | Know Your Customer | 客户身份识别 |
| **AML** | Anti-Money Laundering | 反洗钱 |
| **风控模型** | Risk Model | 评估贷款 / 交易风险的模型 |
| **不良率 / 逾期率** | NPL / Overdue Rate | 不能正常还款的比例 |
| **资产质量** | Asset Quality | 资产健康程度 |
| **拨备覆盖率** | Provision Coverage | 准备金占不良贷款的比例 |
| **监管沙盒** | Regulatory Sandbox | 创新业务的监管试点 |
| **持牌经营** | Licensed Operation | 拥有金融牌照才能做的业务 |
| **嵌入式金融** | Embedded Finance | 把金融能力嵌入到非金融场景 |
| **稳定币** | Stablecoin | 与法币挂钩的数字货币 |
| **CBDC** | Central Bank Digital Currency | 央行数字货币 |
| **DeFi** | Decentralized Finance | 去中心化金融 |
| **跨境支付** | Cross-Border Payment | 跨国资金清算 |

---

## 七、游戏 / 娱乐术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **DAU / MAU** | Daily / Monthly Active Users | 日 / 月活跃 |
| **ARPU / ARPPU** | Average Revenue Per User / Paying User | 单用户/付费用户收入 |
| **付费率** | Pay Rate | 付费用户占比 |
| **LTV** | Lifetime Value | 用户生命周期价值 |
| **IAP** | In-App Purchase | 应用内购买 |
| **IAA** | In-App Advertising | 应用内广告变现 |
| **CPI** | Cost Per Install | 单次安装成本 |
| **ROAS** | Return on Ad Spend | 广告投放回报率 |
| **次留 / 7 留 / 30 留** | Day-1 / 7 / 30 Retention | 留存率 |
| **流水** | Gross Revenue | 月流水 / 总流水 |
| **MMO / MOBA / FPS** | 游戏类型 | 大型多人 / 多人在线竞技 / 第一人称射击 |
| **抽卡 / 扭蛋** | Gacha | 概率获取道具的玩法 |
| **PVP / PVE** | Player vs Player / Environment | 玩家对战 / 玩家对环境 |
| **赛季制** | Season Pass | 周期性更新的玩法 |
| **副本 / Boss** | Dungeon / Boss | 关卡 / 终极挑战 |
| **公会 / 战队** | Guild / Clan | 玩家组织 |
| **UGC** | User Generated Content | 用户生成内容 |
| **二次元** | Anime/Game/Comic | 动漫游戏漫画文化 |
| **买断制 / 免费制** | Premium / Free-to-Play | 一次买断 vs 免费下载内购 |

---

## 八、硬件 / 半导体术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **BOM** | Bill of Materials | 物料清单 |
| **NPI** | New Product Introduction | 新品导入 |
| **EMS** | Electronic Manufacturing Services | 电子制造服务（如富士康） |
| **OEM / ODM** | Original Equipment / Design Manufacturer | 代工 / 代设计 |
| **MOQ** | Minimum Order Quantity | 最小起订量 |
| **良率** | Yield | 合格品率 |
| **BOM 成本** | Material Cost | 物料成本 |
| **晶圆** | Wafer | 半导体加工的硅片 |
| **流片** | Tapeout | 芯片设计完成后送去生产 |
| **制程** | Process Node | 5nm / 3nm 等工艺节点 |
| **EDA** | Electronic Design Automation | 芯片设计软件（如 Cadence） |
| **IP 核** | IP Core | 可复用的芯片设计模块（如 ARM） |
| **GPU / NPU / TPU** | 各类专用芯片 | 图形 / 神经网络 / 张量处理单元 |
| **ASIC** | Application-Specific IC | 专用集成电路 |
| **FPGA** | Field-Programmable Gate Array | 现场可编程逻辑门阵列 |
| **DRAM / NAND** | 存储类型 | 内存 / 闪存 |
| **HBM** | High Bandwidth Memory | 高带宽内存（AI 必备） |
| **TSV** | Through-Silicon Via | 硅通孔（封装技术） |
| **Foundry** | 代工厂 | 如台积电、三星、中芯国际 |

---

## 九、自动驾驶 / 出行术语

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **L0-L5** | SAE 自动驾驶分级 | L4 高度自动 / L5 完全自动 |
| **ADAS** | Advanced Driver Assistance Systems | 高级辅助驾驶 |
| **LiDAR** | Light Detection and Ranging | 激光雷达 |
| **HD Map** | High Definition Map | 高精度地图 |
| **V2X** | Vehicle to Everything | 车与万物互联 |
| **OTA** | Over-the-Air | 远程在线升级 |
| **E/E 架构** | Electrical/Electronic Architecture | 整车电子电气架构 |
| **域控制器** | Domain Controller | 整合多个 ECU 的中央计算单元 |
| **MPI** | Miles Per Intervention | 多少英里需要人介入一次 |
| **Robotaxi** | 自动驾驶出租车 | 无人化运营的网约车 |
| **MaaS** | Mobility as a Service | 出行即服务 |
| **Take Rate** | 抽佣率 | 平台抽成（与支付不同语境） |
| **DAU / WAU** | Daily / Weekly Active Users | 日活 / 周活 |
| **应答率** | Response Rate | 司机接单的比例 |
| **完单率** | Completion Rate | 订单成功完成的比例 |

---

## 十、销售 / 商业通用术语（任何 ToB 销售岗都需要）

| 术语 | 全称 | 通俗解释 |
|------|------|----------|
| **KA** | Key Account | 重点 / 大客户 |
| **SMB** | Small and Medium Business | 中小客户 |
| **ToB** | To Business | 面向企业 |
| **ToC** | To Consumer | 面向个人 |
| **ToG** | To Government | 面向政府 |
| **MQL** | Marketing Qualified Lead | 市场合格线索 |
| **SQL** | Sales Qualified Lead | 销售合格线索 |
| **SDR** | Sales Development Rep | 销售开发代表（找线索） |
| **AE** | Account Executive | 销售代表（签单） |
| **CSM** | Customer Success Manager | 客户成功经理（保续费） |
| **AM** | Account Manager | 客户经理（维护关系） |
| **Pipeline** | 销售漏斗 | 从线索到签约的所有进行中机会 |
| **Win Rate** | 赢单率 | 签约/总机会的比例 |
| **Sales Cycle** | 销售周期 | 从接触到签约的时长 |
| **Quota** | 销售指标 | 个人/团队的业绩任务 |
| **OTE** | On-Target Earnings | 达标后的总收入（底薪+提成） |
| **Commission** | 提成 | 销售按签约额拿的奖励 |
| **POC** | Proof of Concept | 概念验证（小范围试用） |
| **RFP / RFI** | Request for Proposal / Information | 招标邀请 / 信息征询 |
| **MEDDIC / SPIN** | 销售方法论 | 大客户销售常用框架 |
| **决策链** | Decision Chain | 客户内部影响决策的人 |
| **Champion** | 内部支持者 | 客户内部帮你说话的人 |
| **Decision Maker** | 决策者 | 拍板的人（C-level） |
| **Gatekeeper** | 把关者 | 拦在你和决策者之间的人 |
| **Bant** | Budget/Authority/Need/Timeline | 销售线索筛选框架 |

---

## 行业术语生成流程

### 当 AI 调用本文件时：

```
第一步：识别公司行业
- 用户输入「{company}」
- 通过搜索结果，确认主营业务
- 选择 1-2 个最匹配的行业标签

第二步：组合术语
- 从「销售/商业通用」选 5 个（任何岗位都用得上）
- 从该行业的章节选 10-15 个
- 如有公司特定的黑话，补充 2-5 个（如字节的"对齐 / 闭环"）

第三步：插入报告
- 放在简化版报告的「六、行业术语速查表」
- 放在深度版报告的附件里
- 总数控制在 15-25 个，不要堆砌
```

### 公司特定术语的补充

每家公司都有自己的"黑话"，以下举例（可在调研时补充）：

| 公司 | 特色术语 | 含义 |
|------|---------|------|
| 字节跳动 | 对齐 / 闭环 / OKR | 跨部门统一认识 / 完整回路 / 目标管理 |
| 阿里 | 拥抱变化 / 客户第一 | 价值观词汇 |
| 腾讯 | 用户价值 / 灯塔客户 | 价值观 / 标杆客户 |
| Meta | Move Fast / Be Bold | 行动派 / 敢于冒险 |
| Google | 10X Thinking / Moonshot | 十倍思维 / 登月项目 |

---

*Prompt 版本：v3.0（通用版）*
*适用平台：OpenClaw / Cursor*
*更新日期：2026-04-27*
