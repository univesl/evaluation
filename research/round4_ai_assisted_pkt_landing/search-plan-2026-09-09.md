# 2026-09-09 定向复核协议

目的：保存本轮讨论，重新审视 AI 协作编程能力追踪的最近邻，支持未来一至两天的阅读选择，不承诺架构或独占创新。

范围：编程 KT、AI 协作能力评价、过程数据、模拟学生及效度反证。纳入一手论文、作者仓库、数据说明；只使用摘要的条目标记 discovery，不用于细节结论。工业协作仅作邻域参考，不直接外推学生。

检索路径：复用既有 corpus 和 2026-09-07 审查；对 arXiv、ACL Anthology、EDM proceedings、作者数据页定向查证。补充网页发现查询如下，时间范围不强制过滤，以免遗漏经典工作；优先核对 2025–2026。

1. programming knowledge tracing AI collaboration student assessment longitudinal 2026（直接重合）
2. human AI coding proficiency assessment longitudinal students（构念与测量）
3. student simulation programming BEAGLE conversational serialization（合成数据方法）
4. AI assisted programming knowledge tracing systematic review（综述与遗漏方向）

停止规则：本轮为有界刷新，不宣称系统综述饱和；保存返回结果与重要原文定位。下一轮连续两次扩展不再新增构念/方法/效度风险后，才考虑该分支饱和。无结果、访问失败与未检索分别记录。

证据标签：EVIDENCE 为原文事实；INTERPRETATION 为综合判断；HYPOTHESIS 为尚待验证的设想。论文存在、代码开放、学生数据可合法使用是三个独立判断。

## 实际执行与筛选

- 网页发现执行上述四条查询，并定向打开 arXiv、ACL Anthology、EDM 与作者仓库，关键来源和定位见文献地图与 evidence-update-2026-09-09.csv。
- 索引查询 `AI assisted programming knowledge tracing collaboration assessment`，2024 起，每源最多 10 条，openalex/semantic-scholar/arxiv。运行日期 2026-09-09；本地缓存 `research/search/runs/20260909T005021+0800_ai-assisted-programming-knowledge-tracing-collabor-5e57a7a.json`。
- arXiv 返回 6 条去重结果；OpenAlex 与 Semantic Scholar 均 HTTP 429，属于失败而非零结果。全库新增 1 条元数据不代表新增 1 篇核心文献。
- 六条索引结果均未进入本轮核心证据：2405.14107 特征工程（邻域但非学生评价）；2601.14235 天文；2504.15894 医疗决策；2603.28944 决策心理实验；一条 AI 伦理传播研究；2501.02842 信息检索。均为标题/摘要阶段 X-SCOPE，不作质量否定。原始返回缓存保留。
- 关键证据来自既有种子、原文复核和作者文档追溯。新增代码理解综述 DOI 10.1145/3785366 只核到出版商作者摘要，直接页面访问失败，不能报告全文细节。
- 本轮补查了 vibe coding 论文的参考文献入口，以及 TutorTrace 论文指向的 uist 数据说明。前向引文覆盖与 C 方向测量不变性检索仍不足，未达到双轮饱和。
