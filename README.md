# intent-helper

统一的意图管理入口。覆盖意图识别与澄清、意图文档编写、意图执行、测试验证、公共内容维护。

## 这是什么

一个 OpenCode Skill，帮助开发者把模糊需求转化为 AI 能准确执行的意图。核心是四个原则：意图完整、显式化、冗余剪裁、呈现友好。

## 怎么用

把 `intent-helper` 目录放到 `.opencode/skills/` 下。用户提出需求后，AI 自动判断模式：

- **轻量执行**：澄清后直接执行，不生成文档
- **文档模式**：沉淀为意图文档，完善后再实施

## 文件结构

```
intent-helper/
├── SKILL.md              # 总入口
├── methodology.md        # 方法论原文
└── references/           # 各环节详细规则
    ├── clarification.md  # 澄清规则
    ├── writing.md        # 意图文档编写
    ├── executing.md      # 意图执行
    ├── verification.md   # 测试验证
    ├── wiki.md           # Wiki 统一入口
    └── wikis/            # 各子 wiki 实现
        ├── conventions.md
        └── table.md
```

## 依赖的目录

运行时会用到这些项目内目录：

- `.project-info/coding/` — 意图文档
- `.project-info/wikis/` — 项目层知识库
- `.project-info/test-data/` — 测试数据

以及用户层目录：

- `~/.config/intent-helper/wikis/` — 用户层知识库（环境信息、个人知识库）

## 方法论

详见 [methodology.md](./methodology.md)。

## License

MIT
