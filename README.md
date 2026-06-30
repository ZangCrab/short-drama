# 微短剧剧本创作 Skill（项目内副本）

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

## 许可

见本目录 **`LICENSE`**（MIT）。
