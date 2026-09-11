# Round4 研究材料与日期快照规则

本目录同时保存当前定位、历史方案、数据集评估和证据更新。它不是按文件修改时间判断当前状态的；当前入口只由 `research/state.json` 的 `current_archive`、`current_review` 和 `current_authority` 指定。

## 日期快照规则

- 日期命名的研究文档一旦被 manifest、实验记录或远端提交引用，就视为不可变快照。
- 研究定位发生变化时，创建新的 `YYYY-MM-DD` 文档，不直接修改旧日期文件。
- 创建新快照后，依次更新 `state.json` 当前入口、`EXPERIMENT.md` 当前摘要、`experiments/registry.csv`（如影响实验顺序）和 `research/decision-log.md`。
- 旧快照保留用于追溯；如发现错误，新增 dated erratum 或新快照，不改旧 manifest 的哈希来掩盖字节变化。

## 当前快照

当前是哪一版不在本 README 中硬编码，以 `research/state.json` 为准。新设备恢复时先读取 state，再打开它指向的日期文档。

## 历史材料

2026-08-24 落地方案和 2026-09-07 方向评估均为历史版本。它们可以解释研究路线如何变化，但与当前入口冲突时不执行其中的旧计划。
