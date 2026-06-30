# 微短剧剧本创作 Skill（项目内副本）

本目录为 [short-drama](https://github.com/papinoyt15/short-drama) 技能包的本地拷贝，用于在 AI 助手中按流程完成 50–100 集微短剧剧本创作。

## 以谁为准

- **命令、输出文件、自检格式、参考文档加载时机**：一律以本目录下的 **`SKILL.md`** 为准。
- 本 `README` 只做快速索引与使用约定，不重复定义与 `SKILL.md` 冲突的规则。

## 目录结构

```
short-drama/
├── LICENSE                 # MIT（与上游保留一致即可）
├── README.md               # 本说明
├── SKILL.md                # 技能入口（必读）
└── references/             # 按命令阶段加载的知识库
    ├── genre-guide.md
    ├── opening-rules.md
    ├── paywall-design.md
    ├── rhythm-curve.md
    ├── satisfaction-matrix.md
    ├── villain-design.md
    ├── hook-design.md
    └── compliance-checklist.md
```

## 创作产物放哪里（工作目录）

`SKILL.md` 中的 `{项目目录}` 指**你选定用于放剧本与状态文件的那一个根目录**，建议在对话里先约定好其一：

| 约定 | 说明 |
|------|------|
| **仓库根目录**（如 `ThreeDemons/`） | `creative-plan.md`、`.drama-state.json`、`episodes/` 等与 Flutter 代码并列；适合「本仓库就是剧本项目」。 |
| **`short-drama/` 子目录** | 上述文件全部生成在 `short-drama/` 下；适合「剧本与代码隔离」。 |

选定后，让助手始终在同一目录读写，避免状态与分集文件分散两处。

## 命令流程（速查）

在已阅读或附带 `SKILL.md` 的会话中，按顺序使用文档内定义的斜杠指令即可，典型顺序为：

```
/开始 → /创作方案 → /角色开发 → /目录 → /分集 1 → … → /自检 … → /合规（国内）→ /导出
```

- 海外市场：使用 **`/出海`** 或在一开始选择 English（见 `SKILL.md`）。
- **`/自检`**：按 `SKILL.md` 输出评分与修改建议；不要求单独 `reviews/` 目录（除非团队自行约定存档）。

## 参考文档何时加载（与 SKILL.md 一致）

| 参考文件 | 加载时机（命令） |
|----------|------------------|
| genre-guide.md | `/开始` |
| opening-rules.md | `/创作方案`，`/分集`（第 1 集重点） |
| paywall-design.md | `/创作方案`，`/目录` |
| rhythm-curve.md | `/创作方案`，`/分集` |
| satisfaction-matrix.md | `/创作方案`，`/分集` |
| villain-design.md | `/角色开发` |
| hook-design.md | `/分集` |
| compliance-checklist.md | `/合规` |

## 在 Cursor 中怎么用

1. 仓库已配置 **项目规则**：`.cursor/rules/short-drama-screenplay.mdc`。在编辑剧本相关路径（如 `short-drama/`、`episodes/`、`creative-plan.md` 等）或用户明确发出微短剧指令时，助手应 **自动** 按该规则与 `SKILL.md` 执行。
2. 需要显式强调时，在对话里 **@** `short-drama/SKILL.md` 或写明「按微短剧规则执行」。
3. 执行到某一步时，助手须 **`read_file`** 加载 `references/` 下该步要求的 md，再生成内容（与 `SKILL.md` 一致）。

## Cursor 项目规则（强制执行摘要）

| 文件 | 职责 |
|------|------|
| `.cursor/rules/short-drama-screenplay.mdc` | SKILL 流程、references 加载、目录/单集硬性指标 |
| `.cursor/rules/three-demons-drama-bible.mdc` | 《三妖西行记》世界观、角色、坐骑规则、合规、协作与路径 |

**细则模板仍以 `SKILL.md` 为准**；本剧额外设定以 **圣经** 为准，二者须同时遵守。

## 许可

见本目录 **`LICENSE`**（MIT）。
