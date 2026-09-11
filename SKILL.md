---
name: intent-helper
description: 统一的意图管理入口。覆盖意图识别与澄清、意图文档编写、意图执行、测试验证、公共内容维护。
---

# Intent Helper

## Why

解决AI协作中信息传递不完整、不精确的问题——把意图说清楚，让AI能准确执行。


## 核心原则

本 Skill 遵循方法论（[methodology.md](./methodology.md)）的四原则：
- **意图完整**：Why / What / How，用 5W1H 按需填充
- **显式化**：把 AI 不知道的明确告诉它
- **冗余剪裁**：去掉 AI 已知的，保留必要的
- **呈现友好**：核心前置，总分结构，对 AI 和人同样友好


## 模式判断（入口）

用户提出需求后，首先判断：

> **"这是一个一次性任务，还是需要沉淀为意图文档？"**

- **轻量执行**（无文档）：澄清后直接执行 → 见 [references/executing.md](./references/executing.md)
- **文档模式**：沉淀为意图文档，完善后再实施 → 见 [references/writing.md](./references/writing.md)

**进入任一模式时，AI 在对话中先说这句话，然后立即继续推进（澄清、出草稿或直接执行）**：

> "我们一起把这件事理清楚。有不清楚的我会问，你随时补充。"


## 公共内容联动

涉及公共内容时，按 [references/wiki.md](./references/wiki.md) 的统一规则处理。

**查阅方式**：先读项目层总览和用户层总览，再按需读取细节。
- 项目层总览：`.project-info/wikis/总览.md`
- 用户层总览：`~/.config/intent-helper/wikis/总览.md`

**规则**：查阅、引用、维护、提醒，对两层都适用。
- **引用**：意图文档中通过相对路径引用，不复制内容
- **维护**：发现需要新增或修改的内容，引导用户确认后维护
- **提醒**：发现内容过时、多余、不符合四原则、需要纳入，或内容不适合放项目层（含敏感信息）→ 主动提醒


## 职责索引

| 环节 | 详见 |
|------|------|
| 意图识别与澄清 | [references/clarification.md](./references/clarification.md) |
| 意图文档编写 | [references/writing.md](./references/writing.md) |
| 意图执行 | [references/executing.md](./references/executing.md) |
| 测试验证 | [references/verification.md](./references/verification.md) |
| Wiki | [references/wiki.md](./references/wiki.md) |
| 公共约定维护 | [references/wikis/conventions.md](./references/wikis/conventions.md) |
| 表结构维护 | [references/wikis/table.md](./references/wikis/table.md) |


## 注意事项

- **变更记录由 Git 负责**：意图文档内不保留历史变更痕迹
- **公共内容遵循剪裁原则**：只写项目特有规则，不写 AI 已知常识
- **公共内容联动遵循 wiki.md**：查阅、引用、维护、提醒，对两层都适用
- **所有引用使用相对路径**：确保目录迁移后仍然有效
- **总-分结构按复杂度自然浮现**：不强求一开始定好结构，随意图梳理逐步调整
- **呈现友好**：结构对 AI 和人同样友好，核心信息靠前，总览与细节分离
