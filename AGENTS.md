# AGENTS.md

本文件适用于整个仓库，保存跨设备、跨会话长期有效的项目规则。聊天记录不是项目状态来源。

## 1. 新会话的必读顺序

在分析、改代码或运行实验前，依次读取：

1. `AGENTS.md`
2. `EXPERIMENT.md`
3. `experiments/registry.csv`
4. `research/state.json`
5. `research/decision-log.md` 的最新条目
6. `research/round4_ai_assisted_pkt_landing/研究计划落地完善与数据集评估_2026-08-24.md`

随后检查 `git status --short --branch` 和最近提交。先用几句话复述当前阶段、阻塞项和拟执行工作；若状态文件与代码/产物冲突，以可验证文件为准并先修正状态记录。

## 2. 项目目标与研究边界

核心问题：在控制题目、KC、当前代码、正确性、测试与历史表现后，AI 交互是否包含对后续独立表现的增量信息；若有，信息主要来自使用强度，还是采纳、修改、拒绝和验证等行为。

贡献按以下顺序建立：

1. 观测增量性：AI 交互证据是否稳定有效。
2. 表示增量性：行为/语义表示是否优于次数、时长等简单统计。
3. 状态建模增量性：只有前两级通过后，才考虑 AI-aware adaptor 或新 KT 架构。

回顾性数据主要支持预测与关联，不能把历史自选择的 AI 使用解释为学习因果效应。系统生成的掌握度也不能作为独立学习真值。

## 3. 目录职责

- `research/round4_ai_assisted_pkt_landing/`：当前研究方案与数据集评估的可共享权威版本。
- `research/state.json`：机器可读的研究阶段、候选方向和开放问题。
- `research/decision-log.md`：追加式的重要研究决策；不要改写历史条目。
- `output/documents/`：面向导师或合作者的审阅版文档。
- `experiments/registry.csv`：所有重要实验和里程碑的索引。
- `experiments/configs/`：冻结的实验配置；运行后不得就地改写。
- `experiments/results/`：小型、结构化结果摘要，不保存完整日志或模型。
- `experiments/notes/`：结论、异常、失败原因和复现实务说明。
- `experiments/data-manifests/`：去标识的数据版本、哈希、schema 与授权说明。
- `evaluate/`：本机数据库导出工具，可能包含内部配置；整个目录不纳入 Git。
- `retrieved_data/`：本地学生级数据；整个目录不纳入 Git。
- `tmp/`、`.tmp*/`：临时渲染、抽取和下载结果；不纳入 Git。

## 4. 当前环境与运行方式

当前仓库尚无训练入口、统一环境锁文件或自动化测试套件。不要虚构训练命令。正式进入 E1 前，需要增加可复现环境声明、数据适配器、基线入口和测试。

现有本地导出脚本使用 Python 与 PyMySQL，并依赖只在合规网络和授权设备上可用的数据库。数据库导出和验证不是普通的跨设备恢复步骤；运行前必须得到用户确认并检查本机环境变量。

当前可安全执行的仓库检查：

```powershell
git status --short --branch
git log -5 --oneline
git ls-files
```

## 5. 实验生命周期

重要实验 ID 使用 `EYYYYMMDD-NNN-short-name`；非模型里程碑可用 `MYYYYMMDD-NNN-short-name`。状态只能使用：`planned`、`running`、`completed`、`failed`、`aborted`、`blocked`。

开始实验前：

1. 在 `experiments/registry.csv` 登记 ID、目标和状态。
2. 从模板创建 `experiments/configs/<id>.yaml`，冻结随机种子、特征层、模型、切分、指标和资源预算。
3. 创建或引用 `experiments/data-manifests/<data-id>.yaml`，记录哈希、schema、过滤规则和权限；不写 PII 或真实本地绝对路径。
4. 记录代码提交；工作区脏时不得把结果标为可复现基准。

实验结束后：

1. 将小型指标写入 `experiments/results/<id>.json`。
2. 将结论、异常、失败原因和产物位置写入 `experiments/notes/<id>.md`。
3. 更新 registry 的状态、提交、时间和路径。
4. 只有实际影响当前判断的实验或里程碑，才在 `EXPERIMENT.md` 增加一行摘要。
5. 若产生新的长期规则，同步更新 `AGENTS.md`。

不得只在聊天中宣告实验成功。没有配置、数据 manifest、代码提交和结果摘要的运行，不进入正式结论。

## 6. 结果与日志规范

- Git 中只保存小型、可读、可比较的指标摘要和图表；完整日志、checkpoint、缓存和大型中间特征保存在 Git 外。
- 外部产物在 notes 中记录逻辑 URI、生成时间、SHA-256 和保留策略，不记录含用户名的本地绝对路径。
- 主指标优先使用 Log Loss、Brier score 和校准；同时报告 AUROC，类别不平衡时报告 AUPRC。
- 统计单位以学生为主，使用学生级 bootstrap 或层级方法；禁止把相邻提交随机拆到训练和测试。
- 结果必须同时报告绝对性能、相对基线的增量、95% 区间，以及学生/题目/事件数。

## 7. 数据与安全规则

- 绝不提交学生姓名、学号、完整对话、源代码提交、考试明细、原始身份映射、数据库快照或导出文件。
- 绝不在代码、Markdown、配置、registry、日志或提交信息中保存 API Key、Token、密码、私钥或内部数据库连接信息。
- `.env` 只存本机且必须被忽略；仓库只能提供空值示例。
- “没有 AI 日志”必须区分未使用与未采集；缺失原因进入 schema。
- 本地数据只允许生成聚合审计或去标识 manifest 后进入仓库。
- 发现凭据曾硬编码时，不要把文件加入 Git，并提醒用户轮换凭据。

## 8. 不得随意修改的内容

- 不改写 `research/decision-log.md` 既有历史，只能追加更正或新决策。
- 不覆盖已完成实验的冻结配置；需要变更时创建新实验 ID。
- 不把 `research/state.json` 中的阶段提升为 `running` 或 `completed`，除非存在对应实验记录和产物。
- 不删除原始研究计划或经过审阅的输出文档。
- 不移动、重命名或清洗本地数据，除非用户明确授权并确认备份与目标路径。

## 9. Git 与跨设备同步

- 开始工作前先拉取并查看状态；避免在两台设备上同时改同一个实验配置。
- 提交应按“状态/文档”“代码”“单个实验结果”分开，提交信息写清实验 ID。
- 未经用户明确要求，不执行 `git push`、强制推送、历史重写或删除远端分支。
- 合并冲突时，registry 和 `EXPERIMENT.md` 需要语义合并，不能简单选择一侧覆盖。
- Git 不负责同步私有数据；另一台设备必须通过批准的安全渠道取得同一数据版本，并核对 manifest/hash。
