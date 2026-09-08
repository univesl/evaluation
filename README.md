# 面向 AI 辅助编程的学习者能力观测与动态追踪

探索明确 AI 工具条件下的纵向协作编程能力，后续 AI 辅助新任务表现为主，独立编程/代码理解为辅助。创新尚未确定，当前先用一至两天阅读最近邻；保留纵向预测、行为测量、跨工具评价三条假设。

当前为 **E0 / explore**，无运行模型实验、无性能结果。旧计划保留追溯。

当前唯一研究入口：[讨论归档与跨设备接续](research/round4_ai_assisted_pkt_landing/讨论归档与跨设备接续_2026-09-09.md)；[文献地图与阅读决策](research/round4_ai_assisted_pkt_landing/文献地图与阅读决策_2026-09-09.md)。2026-08-24 落地稿和 2026-09-07 方向评估保留为历史追溯，不代表当前研究定位。

## 仓库中包含什么

- `面向 AI 辅助编程的学习者能力观测与动态追踪研究.pdf`：原始研究计划。
- `output/documents/`：经过排版校验的研究建议 Word 文档。
- `research/round4_ai_assisted_pkt_landing/`：当前定位、历史方案、数据集决策矩阵、本地数据聚合审计和检索计划。
- `research/state.json`、`research/decision-log.md`：研究方向状态和重要决策历史。
- `experiments/`：实验登记表、配置/结果/笔记模板及后续实验摘要。

## 仓库中不包含什么

学生级数据、姓名/学号、完整对话、源代码提交、数据库导出、数据库脚本与凭据、临时渲染文件、下载的论文全文、大型模型文件和完整运行日志均不进入 Git。它们只能通过合规的独立渠道在设备间传输。

## 在新设备上恢复上下文

```powershell
git clone https://github.com/univesl/evaluation.git
cd evaluation
git status --short --branch
```

然后让新的 Codex 会话先读取 `AGENTS.md`、`EXPERIMENT.md`、`experiments/registry.csv`、`research/state.json`、2026-09-09 讨论归档和文献地图，再汇报当前阶段与下一步，不要直接运行实验。

## 重要提醒

Git 只同步可共享的研究状态，不同步本地数据。开始任何实验前，必须单独确认数据版本、哈希、权限、字段字典、切分方案和运行环境；不同设备不能仅凭文件名假设使用了同一份数据。
