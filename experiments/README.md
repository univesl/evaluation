# 实验登记目录

本目录保存可共享、轻量、可复现的实验元数据，不保存原始学生数据、完整日志、checkpoint 或大型中间产物。

## 结构

```text
experiments/
├── registry.csv          # 全部实验的唯一索引
├── configs/              # 每个实验的冻结 YAML 配置
├── data-manifests/       # 去标识数据版本、哈希、schema、权限说明
├── results/              # 小型 JSON 指标摘要
└── notes/                # 结论、异常、失败原因和外部产物位置
```

命名统一使用实验 ID，例如：

```text
E20260826-002-public-pkt-baseline
```

同一 ID 的配置、结果和笔记必须对应。已运行配置不得覆盖；参数变化需要新 ID。`EXPERIMENT.md` 只汇总影响当前研究判断的条目。

大型产物保存在 Git 外，并在 notes 中记录逻辑位置、SHA-256、生成时间和保留策略。不得写入用户名、本机绝对路径或任何敏感凭据。
