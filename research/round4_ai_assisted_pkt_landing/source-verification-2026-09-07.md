# 来源核验记录（2026-09-07）

只保存公开元数据与概括，不含学生级记录。全文定位与解释见 evidence-update-2026-09-07.csv。

| ID | 来源 | 核验层级与结论 |
|---|---|---|
| S01 | https://arxiv.org/html/2503.07928v4 | 最终使用v4全文；§4.1增量分析、图3考试标签、§3标签评审。v3仅用于版本追溯。 |
| S02 | https://huggingface.co/datasets/wmcnicho/StudyChat | 数据卡v1.1，文件访问须登录/接受联系信息共享条件；未代替用户接受。 |
| S03 | https://arxiv.org/html/2608.26184v1 | 全文表1、§7.4、§9；480人与4部署为论文口径。 |
| S04 | https://vizpi.org/dataset | 直接抓取仅JS壳；检索引擎返回官方页面正文，664人与8部署为网页口径。当前下载文件未验证。 |
| S05 | https://github.com/umass-ml4ed/tiktoc | README数据说明与目录；无AI；17题；未执行。 |
| S06 | https://github.com/umass-ml4ed/progFeed-dataset-public | README分配/展示区别；字典定义函数/测试行；未读取学生代码。 |
| S07 | https://aclanthology.org/2025.acl-long.1343.pdf | SQKT全文图1和§3；代码之外提问语义已是近邻。 |
| S08 | https://github.com/holi-lab/SQKT | README四表schema可见；递归树API返回403，不能据此判定无数据。 |
| S09 | https://aclanthology.org/2026.bea-1.43.pdf | 全文§4.1：QATD2k/MathDial及LLM标签，属于方法邻域。 |
| S10 | https://aclanthology.org/2025.findings-acl.642.pdf | 全文可访问；摘要确认TRAVER/DICT，受控学生模拟。 |
| S11 | https://arxiv.org/html/2601.20245v1 | §4.3、§5.2、附录B；主试验52人，与pilot区分。 |
| S12 | https://github.com/safety-research/how-ai-impacts-skill-formation | 仓库说明任务与标注记录可见；未确认完整成绩联结表/许可。 |
| S13 | https://portal.fis.tum.de/en/publications/less-stress-better-scores-same-learning-the-dissociation-of-perfo/ | 机构摘要核验275人分析与任务/知识结果分离；出版商全文此次抓取失败，不报告精确效应量。 |
| S14 | https://zenodo.org/api/records/20285307 | 公开元数据确认原始去标识CSV文件、open、CC BY4.0。读取README；未下载学生数据。 |
| S15 | https://zenodo.org/records/20285307/files/README.md?download=1 | HTTP直接读取成功。无Iris消息内容；README清洗表“已附”与API文件清单不符，需生成。 |
| S16 | https://arxiv.org/html/2604.10400v1 | 作者稿摘要与全文可见；163人、prompt轨迹/代码比较。 |
| S17 | https://dblp.dagstuhl.de/rec/journals/corr/abs-2604-10400.html | DBLP元数据确认作为CoRR条目，未将其当正式期刊论文。 |

## 执行与限制

- 三索引精确查询：AI assisted programming knowledge tracing dialogue independent performance；2024起；每源最多15；arXiv成功，返回4条去重记录、全库新增1；OpenAlex与Semantic Scholar 429。
- 原始索引运行：research/search/runs/20260907T003323+0800_ai-assisted-programming-knowledge-tracing-dialogue-62dd44e.json。
- 网页/原始工具响应：本地 research/search/runs/20260907_web-verification-1.json 至 -9.json；不纳入Git。公开信息不等于已允许重新分发数据。
- 已执行Q2–Q4的网页定向检索及SQKT、prompt trajectory、TutorTrace规模冲突追溯。无年份硬过滤的网页查询以2025/2026关键词定位，未将时间标签当正式出版日期。
- 候选筛选保留直接学习者证据/关键方法近邻；产业生产率、纯代码生成、新闻、论坛及第三方论文概述不用于核心论证。综述只作发现线索。
- 新增课堂试验包构念不符核心AI语义任务，保留辅助（不是质量排除）；SQKT与Skill Formation的数据访问只保留未核验，不解释为不可获得。
- 未达到连续两轮无新增的停止标准；这是有限定向更新，不声称穷尽。当前信息已足以支持“先审计、再决定方法”的建议，新颖性仍需投稿前复核。

