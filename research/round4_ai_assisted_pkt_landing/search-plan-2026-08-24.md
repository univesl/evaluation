# AI-assisted Programming KT 数据集与落地方案检索计划

检索日期：2026-08-24（Asia/Shanghai）

## 决策陈述

我们需要在“公开 Programming KT 基线数据、本地多平台纵向数据、公开 Human-AI 编程交互数据、前瞻性自采数据”之间做组合选择，使研究既能验证 Human-AI interaction 的增量预测效度，又不把数据采集、表示学习和新 KT 架构同时变成首轮实验的致命负担。

## 核心问题

1. 哪些公开数据提供稳定 learner ID、题目/知识组件、按时间排序的多次尝试、代码快照、测试结果和后续表现？
2. 哪些公开数据提供 Prompt、AI response、代码采纳/修改、运行/测试/验证事件，并允许跨任务追踪同一学习者？
3. CodeWorkout 及其 OKT/TIKTOC/KCGen-KT 衍生版本分别能支持哪些基线，不能支持哪些核心主张？
4. ProgSnap2、Blackbox、Project CodeNet、ASSISTments/EdNet、DevGPT、RECAP/课堂 AI assistant 数据分别能承担复现、预训练、外部验证、交互表征或因果研究中的什么角色？
5. 本地数据相对公开数据补上了什么，又缺失哪些使核心假设无法识别的关键字段？

## 评价维度

- 人群与情境：真实学习者/开发者、课程类型、任务难度、AI 使用制度。
- 纵向性：稳定 learner ID、跨任务跨度、每人序列长度、时间戳粒度。
- 传统 PKT 证据：problem、KC、correctness、source code、attempt、test case、error/diagnosis。
- AI 交互证据：prompt、response、模型/版本、采纳/拒绝、编辑 diff、运行/测试、验证、对话消息级时间。
- 外部效标：独立作业/考试、无 AI 迁移、延迟保持、debugging/verification、教师评分。
- 可连接性：跨平台 learner key、task key、时间对齐、AI 输出与最终代码的 provenance。
- 访问与复现：公开下载、许可、脱敏、代码/处理脚本、版本稳定性。
- 主要偏差：自选择 AI 使用、遥测缺失、标签泄漏、平台/题目身份泄漏、学生级切分不足。

## 查询族

| ID | 目的 | 查询 | 来源 | 时间/过滤 | 停止规则 |
|---|---|---|---|---|---|
| DS-CW | 核验核心数据 | `CodeWorkout dataset programming knowledge tracing OKT TIKTOC` | ACL Anthology、ACM/LAK、官方仓库、OpenAlex、arXiv | 全时段；优先原论文/仓库 | 数据字段、规模、访问路径和限制均有一手来源 |
| DS-PS | 过程数据邻域 | `ProgSnap2 dataset programming process data code snapshots` | 官方站点/仓库、ICER/EDM、OpenAlex | 2017-2026 | 至少覆盖格式说明和两个公开数据实例 |
| DS-BB | 大规模编程过程 | `Blackbox dataset novice programming event data BlueJ` | 官方站点、论文、仓库 | 全时段 | 核验规模、事件粒度、身份/任务限制 |
| DS-CN | 非教育代码库 | `Project CodeNet dataset submissions metadata status` | IBM 官方、论文/仓库 | 全时段 | 核验其能否支持 learner trajectory |
| DS-KT | 通用 KT 对照 | `ASSISTments EdNet dataset knowledge tracing sequences` | 官方数据页/论文 | 全时段 | 明确只作为方法 sanity check 的边界 |
| DS-AI | AI 编程交互 | `student AI assisted programming interaction dataset prompts code edits` | ACL/CHI/ICSE/LAK/EDM、arXiv、官方仓库 | 2023-2026 | 连续两轮不再出现新字段组合/公开数据 |
| DS-DEV | 开发者对话邻域 | `DevGPT dataset developer ChatGPT conversations GitHub` | MSR/官方仓库 | 2023-2026 | 核验其 population 与纵向能力标签限制 |
| DS-REC | 采集系统 | `RECAP AI-assisted programming interactions dataset code edits prompts` | ACL Anthology/官方仓库 | 2025-2026 | 核验平台是否开放、数据是否开放、可借鉴 schema |

## 纳入/排除标准

纳入：能够承担本研究某个明确实验角色；字段、规模和访问状态可由一手来源核验；限制可被明确写出。排除为核心数据：只有最终代码、没有稳定 learner trajectory；只有题目正确率、没有代码或 AI 轨迹；AI 对话与代码/任务不能关联；无法获得原始数据或许可不清。被排除为核心数据的资源仍可保留为代码编码器预训练、模型实现校验或相邻方法参考。

## 输出

1. 数据集适用性矩阵与分级结论；2. 本地数据字段/质量审计；3. 最小可发表数据组合；4. 补采字段与数据治理清单；5. 分阶段技术路线、实验矩阵、停止/升级条件。
