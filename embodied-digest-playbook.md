# 具身智能日报玩法（对齐 AIHOT 机制）

来源：https://aihot.news/agent · Skill https://github.com/KKKKhazix/khazix-skills/tree/main/aihot

## 从 AIHOT 学到的筛选/处理机制（消费侧契约）
1. **多源聚合 → LLM 摘要 → 打分精选**：公开池 `mode=all`，精选池 `mode=selected`（高门槛）。
2. **关键词冷门回退**：`q` 查 selected 为空时，同参再查 `mode=all`，并标明「未进精选」。
3. **时间轴**：默认 `by=timeline`（与网站一致）；慢推信源以收录日算「今天」。
4. **输出字段**：标题链到 `links.aihot`；人话摘要；有 `reason` 才写「为什么值得看」；重要数字回 `links.original`。
5. **条数克制**：简报 3–8 条；不把 score 擅自重排成排行榜。
6. **无信号沉默**：没有高价值条目就不硬推空报。
7. **许可**：个人/内部非商业免费；不对外转售或批量再分发。

## 具身智能专用查询
优先关键词（逐个查 selected，空则 all）：`humanoid` `机器人` `具身` `VLA` `world model` `Unitree` `Figure` `Physical Intelligence` `人形`。
再合并去重，只留与物理机器人 / Embodied AI / 产线相关的。

## X 补充（省额度）
仅当 AIHOT 过去 24h 具身相关 < 3 条时，才对盯梢名单拉帖（每号最多 3 条、exclude reply/rt）。日预算仍约 $0.50。
名单：`/workspace/learning-map/x-embodied-watchlist.json`
