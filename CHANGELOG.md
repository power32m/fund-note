# 更新记录 / Changelog

## Edge 1.1.2 (2026-10-30)

- 新增本地分时走势，同日统一比例，零线居中，当日范围只扩大不缩小。
- 10分钟以内的小缺口实线衔接，悬停披露缺失时段，不生成虚假点位。
- 修正后台定时重复创建及60秒临界跳过问题；保留手动冷却。
- 自愿打赏、本地CSV备份；简体中文和英文商店配置。
- 此1.1.2包包含此前本地1.1.3—1.1.5迭代的修正，按作者要求统一版本号。

Shared zero-centered intraday scale, solid short-gap connectors with honest gap tooltips, background alarm/cooldown timing fixes, optional support and bilingual store metadata. This consolidated 1.1.2 includes fixes previously labeled 1.1.3–1.1.5 in local iterations.



## Chrome 1.0 测试版 / test build — 1.0.0 (2026-10-30)

- Popup小笺与完整持仓视图；基金行情日收益、确认资产和持仓收益。
- 原图标叠加原生收益角标：盈利红底白字、亏损绿底白字，与面板同步。
- 指数滚动条停留1秒展开，移开渐隐；按市场时段刷新并保护手动请求。
- CSV导入导出、最多10份修改前备份、旧页面覆盖保护、空持仓首次安装。
- 清理失效桌面适配与图标试验代码，完成收益、跨日、CSV和浏览器流程验收。
- 本次发布为本地加载的测试包，尚未上架Chrome Web Store。

English:

- Popup and detailed portfolio views with quote-day returns, confirmed assets and holding returns.
- Original icon plus native red/green background badge, synchronized with the popup.
- One-second hover index panel, fade-out, market-session refresh and manual request cooldowns.
- CSV import/export, up to ten pre-edit snapshots, stale-page write protection and empty fresh installs.
- Removed obsolete desktop hooks and icon experiments; verified calculations, date handling, CSV and browser flows.
- An unpacked test release; not listed in the Chrome Web Store.
