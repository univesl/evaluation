# 面向 AI 辅助编程的学习者能力观测与动态追踪

本仓库保存研究计划、可共享的证据总结和跨设备实验状态。当前核心问题是：在已经控制题目、知识组件、学生代码、正确性和测试证据后，Human–AI interaction 是否仍能提高对学习者后续独立表现的预测。

## 当前阶段

项目处于 **实验前准备 / E0 数据与构念就绪阶段**。研究问题、技术路线、候选数据集和分阶段实验门槛已经形成；尚未开始模型训练，也没有可报告的实验性能结果。

最新状态见 [EXPERIMENT.md](EXPERIMENT.md)，长期协作规则见 [AGENTS.md](AGENTS.md)。

## 仓库中包含什么

- `面向 AI 辅助编程的学习者能力观测与动态追踪研究.pdf`：原始研究计划。
- `output/documents/`：经过排版校验的研究建议 Word 文档。
- `research/round4_ai_assisted_pkt_landing/`：可编辑建议、数据集决策矩阵、本地数据聚合审计和检索计划。
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

然后让新的 Codex 会话先读取 `AGENTS.md`、`EXPERIMENT.md`、`experiments/registry.csv`、`research/state.json` 和最新研究建议，再汇报当前阶段与下一步，不要直接运行实验。

## 重要提醒

Git 只同步可共享的研究状态，不同步本地数据。开始任何实验前，必须单独确认数据版本、哈希、权限、字段字典、切分方案和运行环境；不同设备不能仅凭文件名假设使用了同一份数据。
