# Journal Cleaner - 提炼

从清洗后的日记中提取结构化的事件记忆。

## 前提

先完成清洗步骤，获得清洗后的日记。

## 步骤

### 步骤 1：读取清洗后的日记

从 `default/journal/diary/` 读取当天清洗后的日记。

文件命名格式：`YYYY-MM-DD.md`

### 步骤 2：提取事件记忆

使用 AI 从清洗后的日记中提取事件。

**Prompt**：

```
这是清洗后的日记，我们现在要提取其中的事件记忆

定义 EpisodicMemory 模型：
- id: uuid
- title: str
- description: str
- tense: past | present | future
- type: decision | plan | report | evaluation | retrospective
```

**输出格式**：JSONL（每行一个 JSON 对象）

### 步骤 3：保存文件

保存到 `default/memory/episodic/YYYY-MM-DD.jsonl`

## EpisodicMemory 模型

```json
{
  "id": "uuid",
  "title": "string",
  "description": "string",
  "tense": "past | present | future",
  "type": "decision | plan | report | evaluation | retrospective"
}
```

### `tense` 枚举值
- **`past`**：过去发生的事件
- **`present`**：当前正在发生的事件
- **`future`**：计划中或预期发生的事件

### `type` 枚举值
- **`decision`**：做出的决策
- **`plan`**：制定的计划
- **`report`**：工作汇报
- **`evaluation`**：评估和反思
- **`retrospective`**：回顾
