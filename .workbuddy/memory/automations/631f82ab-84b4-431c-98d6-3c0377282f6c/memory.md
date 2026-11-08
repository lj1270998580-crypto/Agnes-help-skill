# Agnes 官方更新巡检自动化 — 执行记忆

- 自动化 id：631f82ab-84b4-431c-98d6-3c0377282f6c（每天 21:00 触发）
- 职责：巡检 Agnes 官方文档（overview/pricing/tokenplan + WebSearch 公告），有实质性更新则同步 GitHub 技能仓库（lj1270990998580-crypto/Agnes-help-skill，本地 Agnes-help-skill/）与创意空间网页（Desktop + D 盘 + 上传），无更新则直接结束。
- 版本号四处须一致（SKILL.md frontmatter / SKILL.md 正文 / README / API 文档）。

## 最近执行
- 2026-11-07 21:00：检测到官方订阅计划页新增内容（Agent Plan 年付档位、加购 Credits 积分包价格、完整模型折扣系数表）未同步 → 实质性更新。版本 1.3.4→v1.3.5（并修正 API 文档遗留 v1.3.3）。commit 429e2ac，上传 195/195，curl 验证通过。
- 历史：2026-11-07 早些时候已同步 v1.3.3（实名认证公告）、v1.3.4（2026-10-29 订阅体系重构/RPM 动态调整）。
- 截至 2026-11-07，本地已追平官方至 2026-10-29 订阅重构 + 2026-11-07 补充的年付/积分包/折扣；agnes-3.0-pro 仍为「即将上线」未发布。

## 注意
- WebFetch 在沙箱内可能失败，验证线上页需用 dangerouslyDisableSandbox 的 curl（或退出沙箱）。
- 网页 skillKnowledge 模板字符串内不得出现反引号或 ${}。
