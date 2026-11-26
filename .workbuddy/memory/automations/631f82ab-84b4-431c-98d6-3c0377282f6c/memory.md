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

## 最近执行（续 4）
- 2026-11-11 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10）逐条一致：模型列表、USD 价格、RPM、Agent Plan / Token Plan、折扣表、agnes-3.0-pro（仍「即将上线」）均无新增/下线/改价/新公告；国内站 .cn 返回人民币价格（国内站固有币种，非变更）。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。

## 最近执行（续 5）
- 2026-11-12 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10）逐条一致：模型列表、USD 价格、RPM、Agent Plan / Token Plan、折扣表、agnes-3.0-pro（仍「即将上线」）均无新增/下线/改价/新公告；tokenplan 页新增 Credits 使用细则/5 小时窗口/退款声明/Harness API 规划说明与图片尺寸档位表，均属文档细化非实质性变更。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。

## 最近执行（续 6）
- 2026-11-13 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格（agnes-2.5-pro-theta 已 $0.01/$0.10/$0.30、agnes-3.0-pro 仍「即将上线」）均无新增/下线/改价/新公告；WebSearch 仅返回 7-9 月历史文章，无 11 月新官方公告。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-14 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格（agnes-2.5-pro-theta 已 $0.01/$0.10/$0.30、agnes-3.0-pro 仍「即将上线」同档预告）、RPM、Agent Plan / Token Plan、折扣表、积分包价格均无新增/下线/改价/新公告；WebSearch 仅返回历史文章（7-9 月），无 11 月新官方公告。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-15 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + 国内站定价页交叉核对 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格（theta 已 $0.01/$0.10/$0.30、agnes-3.0-pro 仍「即将上线」同档）、RPM、Agent Plan 月/年付、Token Plan 老用户保留、折扣表、积分包价格均无新增/下线/改价/新公告；WebSearch 无 11 月新官方公告（freellm/sovyron 为第三方聚合站非官方）。本地 agnes-2.5-flash 刊例输入价记 $0.03（官方 $0.05）属历史遗留差异、体验价长期 $0 不影响计费，非今日新变化，不改。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-17 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + 国内站定价页交叉核对 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格（theta $0.01/$0.10/$0.30、agnes-3.0-pro 仍「即将上线」同档）、RPM、Agent Plan 月/年付、Token Plan 老用户保留、折扣表、积分包价格、换算基准 6,600 Credits=$1 均无新增/下线/改价/新公告；WebSearch 无 11 月新官方公告（mindber/learncs/freellm/头条均第三方或历史文章，头条提及的 agnes-3.0-flash-max 官方定价页未列，不改）。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-18 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格（theta $0.01/$0.10/$0.30、agnes-3.0-flash 体验价全 $0）、RPM、Agent Plan 月/年付、Token Plan 老用户保留、折扣表、积分包、换算基准均无新增/下线/改价/新公告。核实要点：agnes-3.0-pro 已有独立文档页 agnes-30-pro，但状态明确「Coming soon / 即将上线」、API 未开放、定价 $0.01/$0.10/$0.30（与本地预告一致）；WebSearch 快照中的 $0.045/$0.45/$0.90 为旧缓存、实际页面已订正，非改价。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-19 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview 三页 + 国内站 pricing 交叉核对（¥ 币种，模型集合一致）+ agnes-3.0-pro 模型页（仍「即将上线」、$0.01/$0.10/$0.30）+ WebSearch 公告检索，与本地 v1.3.7（2026-11-10，commit aa4461e）逐条一致：模型列表、USD 价格、RPM、Agent Plan 月/年付、Token Plan 老用户保留、折扣表、积分包、换算基准 6,600 Credits=$1 均无新增/下线/改价/新公告。WebSearch 仅返回第三方媒体对 11-15 theta 开源权重（HF/Apache 2.0/187.8B MoE）的报道，非官方 API 文档变更。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.7。
- 2026-11-20 21:00：**检测到实质性更新，已全量同步**。①官方定价页新增「决策模型」分类 + 独立文档页 agnes-sys1-10：新模型 `agnes-sys1-1.0`（即将上线），专用接口 `POST /v1/systemone`，state+questions 输入 / answers 输出（choice/noul 题型），输入 $0.03/M、输出免费，Agnes Harness 的 9B System 1 决策模型；本地此前无记录。②`agnes-3.0-pro` 定价页由「即将上线」改为「已正式上线」（$0.01/$0.10/$0.30），但独立文档页 agnes-30-pro 仍写「即将上线」，已如实记录口径不一致。③WebSearch 捕获 11-20 官方 Harness/Sys1 1.0 新闻。版本 1.3.7→v1.3.8（四处一致）；commit `0bb1688`（main）；网页 skillKnowledge 更新（公告+新增决策模型分类+3.0-pro 状态）→cp D 盘→upload.js 208/208→curl 线上含 agnes-sys1-1.0（2）/已正式上线（2）通过。
- 巡检方法备注：WebFetch 沙箱内正常抓取 pricing/tokenplan/overview + agnes-sys1-10 + agnes-30-pro；线上 curl 验证需 dangerouslyDisableSandbox。npm 包 `@bitkyc08/opencodex` 无关。新决策模型接口 /v1/systemone 是本次核心新增，区别于所有 /v1/chat/completions 系列。
- 2026-11-21 21:00：**检测到实质性更新，已全量同步**。①官方模型文档 agnes-25-flash + pricing 页发布下线公告：`agnes-2.5-flash` 将于 **2026-11-30** 正式下线，迁移至 `agnes-3.0-flash`（default 免费 / 512K / 65536 输出 / 三端点 + Thinking）；`agnes-2.0-flash` 已废弃不可作回退。②`agnes-sys1-1.0` 在定价页与独立文档页均已改为「已正式上线」（接口/计费不变），官方补录内部自测估算成绩（标注预估、非独立验证）。版本 1.3.8→v1.3.9（四处一致）；commit `371a133`（main）；网页 skillKnowledge 更新→cp D 盘→upload.js 209/209→curl 线上含 2026-11-30 / agnes-sys1-1.0 / 已正式上线 验证通过。其余模型/价格/RPM/订阅无变化；agnes-3.0-pro 维持 11-20 口径（定价页已上线、文档页仍写即将上线）。
- 巡检方法备注：本次 WebFetch 沙箱内抓取 pricing/tokenplan/overview/agnes-sys1-10/agnes-25-flash 全部成功，线上 curl 验证本次沙箱内直接可用（无需 dangerouslyDisableSandbox）。桌面与 D 盘网页源编辑后 SHA256 一致再上传。
- 2026-11-22 21:00：**检测到实质性更新，已全量同步**。官方 `agnes-3.0-pro` 独立文档页（国际站 + 国内站交叉核对）由「即将上线」改为**「已正式上线」**，与定价页口径一致，此前本地三文件记录的「文档页仍写即将上线」口径不一致消除；官方文档补齐 **1M 上下文 / 256K 最大输出**（旧记 65,536，以官方当前 256K 为准），价格不变（$0.01/$0.10/$0.30）。其余模型/价格/RPM/订阅无变化；2.5-flash 维持 11-30 下线、sys1-1.0 维持已上线；WebSearch 无 11-22 新公告。版本 1.3.9→v1.3.10（四处一致）；commit `e193486`（main）；网页 skillKnowledge 两处 3.0-pro 口径更新→cp D 盘（SHA256 一致）→upload.js 210/210→curl 线上含「独立文档页改为已正式上线」/256K 最大输出/2026-11-22 验证通过。
- 巡检方法备注：本次 WebFetch 沙箱内全部成功，线上 curl 验证沙箱内直接可用。内存日志文件位于技能仓库内会被 git 跟踪（git add -A 会带入），注意 LF/CRLF 警告无害。
- 2026-11-23 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview + agnes-30-pro / agnes-sys1-10 / agnes-25-flash 六页 + 国内站 pricing 交叉核对 + WebSearch 公告检索，与本地 v1.3.12（commit ecbf7d0，2026-11-23 当天已人工同步官方通知+修复 issue）逐条一致：模型集合、USD 价格、2.5-flash 11-30 下线、3.0-pro 已上线（1M/256K）、sys1-1.0 已上线（输入 $0.03/M 输出免费）、Agent Plan 月/年付、折扣表、积分包、Token Plan 老用户保留、RPM 动态调整均无新增/下线/改价/新公告。WebSearch 仅返回 11-15～11-19 历史文章（Harness 开源 / theta 开源权重 / 第三方追踪站），无 11-23 新公告。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.12。
- 巡检方法备注：本次 WebFetch 沙箱内全部成功。本地版本已由白天人工更新至 v1.3.12，晚间巡检基准即为此版本（高于此前记忆中的 v1.3.10），注意以 SKILL.md/README/API 文档实际版本为准而非记忆中的旧版本。
- 2026-11-24 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview + agnes-30-pro / agnes-sys1-10 / agnes-25-flash 六页 + WebSearch 公告检索，与本地 v1.3.12 逐条一致：模型集合、USD 刊例价与现价、2.5-flash 11-30 下线、3.0-pro 已上线（1M/256K）、sys1-1.0 已上线（输入 $0.03/M 输出免费）、Agent Plan 月/年付、折扣表、积分包、6,600 Credits=$1、Token Plan 老用户保留、RPM 动态调整均无新增/下线/改价/新公告。WebSearch 仅返回第三方聚合/跑分站（rokoapi/unifybench/benchleader/aidaily/免费模型日报），其中 theta $0.10/$0.30、2.5-flash 11-30 下线均与本地已记录一致，无 11-24 新官方公告。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.12。
- 2026-11-25 21:00：**今日 Agnes 官方无更新**。国际站 pricing / tokenplan / overview + agnes-30-pro / agnes-sys1-10 / agnes-25-flash 六页 + WebSearch 公告检索，与本地 v1.3.12 逐条一致：模型集合、USD 刊例价与现价（2.5-pro $0.045/$0.45/$0.90；beta/theta/3.0-pro 均 $0.01/$0.10/$0.30；Flash 现价 $0）、2.5-flash 11-30 下线、3.0-pro 已上线（1M/256K）、sys1-1.0 已上线（输入 $0.03/M 输出免费）、Agent Plan 月/年付、折扣表、积分包、6,600 Credits=$1、Token Plan 老用户保留、RPM 动态调整均无新增/下线/改价/新公告。WebSearch 仅返回第三方聚合/跑分站与历史文章（sovyron 11-24/rokoapi 11-24/franklineh/eogee 周报/11-19 微信），无 11-25 新官方公告。按规则结束，未改文件、未提交、未上传；技能仓库维持 v1.3.12。
