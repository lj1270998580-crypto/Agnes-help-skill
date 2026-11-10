# Agnes 官方更新巡检自动化 — 执行记忆

- 自动化 id：631f82ab-84b4-431c-98d6-3c0377282f6c（每天 21:00 触发）
- 职责：巡检 Agnes 官方文档（overview/pricing/tokenplan + WebSearch 公告），有实质性更新则同步 GitHub 技能仓库（lj1270990998580-crypto/Agnes-help-skill，本地 Agnes-help-skill/）与创意空间网页（Desktop + D 盘 + 上传），无更新则直接结束。
- 版本号四处须一致（SKILL.md frontmatter / SKILL.md 正文 / README / API 文档）。

## 最近执行
- 2026-11-07 21:00：检测到官方订阅计划页新增内容（Agent Plan 年付档位、加购 Credits 积分包价格、完整模型折扣系数表）未同步 → 实质性更新。版本 1.3.4→v1.3.5（并修正 API 文档遗留 v1.3.3）。commit 429e2ac，上传 195/195，curl 验证通过。
- 历史：2026-11-07 早些时候已同步 v1.3.3（实名认证公告）、v1.3.4（2026-10-29 订阅体系重构/RPM 动态调整）。
- 截至 2026-11-07，本地已追平官方至 2026-10-29 订阅重构 + 2026-11-07 补充的年付/积分包/折扣；agnes-3.0-pro 仍为「即将上线」未发布。

## 最近执行（续）
- 2026-11-08 21:00：**检测到官方定价页新增付费推理模型 `agnes-2.5-pro-theta`**（刊例价与 agnes-2.5-pro 相同：$0.045/$0.45/$0.90，暂无独立文档页）→ 实质性更新。版本 1.3.5→v1.3.6（四处一致）；commit `1e4a2fd`（main）。同步技能仓库三文件 + 创意空间网页（桌面源→D 盘源→upload.js 196/196→curl 验证线上含关键词 2 处匹配）。agnes-3.0-pro 仍为「即将上线」未发布。
- 巡检方法备注：WebFetch 在沙箱内可正常抓取官方文档（本次 pricing/tokenplan/overview 均成功）；线上页 curl 验证需用 dangerouslyDisableSandbox。 Agnes 2.5 Pro 系列现含 pro/beta/alpha/theta 四款付费推理模型（theta 与 pro 同价）。

## 最近执行（续 2）
- 2026-11-09 21:00：**今日 Agnes 官方无更新**。官方 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.6 完全一致（模型/价格/RPM/订阅/公告无新增、下线、改价、新公告）；agnes-3.0-pro 仍「即将上线」。官方 tokenplan 仅新增图片 ratio→像素对照表、Harness API 规划说明与折扣「限时」基准标注，均属文档细化非实质性变更。按规则结束，未改文件、未提交、未上传。技能仓库维持 v1.3.6（2026-11-08）。

## 最近执行（续 3）
- 2026-11-10 21:00：**检测到官方定价页实质性改价**。agnes-2.5-pro-theta 刊例价由 pro 档（$0.045/$0.45/$0.90）下调至与 pro-beta / 即将上线的 agnes-3.0-pro 同档（$0.01/$0.10/$0.30，输入成本降约 78%）；同时订正 agnes-3.0-pro（即将上线）预览刊例价（旧 $0.045/$0.45/$0.90 → 官方现 $0.01/$0.10/$0.30）。版本 1.3.6→v1.3.7（四处一致）；commit `aa4461e`（main）。同步技能仓库三文件 + 创意空间网页（桌面源→D 盘源→upload.js 198/198→curl 验证线上含「agnes-2.5-pro-theta 价格调整」关键词）。另将三文件模型折扣表补全为「基础折扣（限时促销折扣）」格式以对齐官方页。
- 巡检方法备注：WebFetch 沙箱内正常；线上 curl 验证用 dangerouslyDisableSandbox。本次为官方定价页主动调价（非独立公告），本地据此同步。

## 注意
- WebFetch 在沙箱内可能失败，验证线上页需用 dangerouslyDisableSandbox 的 curl（或退出沙箱）。
- 网页 skillKnowledge 模板字符串内不得出现反引号或 ${}。
