# 隐私说明 / Privacy policy

适用范围：基金小笺 Chrome 扩展1.0测试版。生效日期：2026-10-30。

## 中文

**本地数据。** 基金代码、名称、份额、成本、缓存、请求时间和最近10次修改前备份保存在 `chrome.storage.local`。不设置软件账号、云同步、作者服务器统计、广告跟踪或网页内容/浏览历史采集。本地存储并非加密保险箱，能访问设备或浏览器配置的人可能接触数据。

**网络请求。** 行情仅请求 `hq.sinajs.cn` 与 `fundmobapi.eastmoney.com`，发送基金/指数代码与固定接口参数，不发送持有份额和成本。服务方可能获得IP地址、请求时间、客户端标识和常规连接信息，依其规则处理。用户主动打开GitHub页面或下载文件时，也适用GitHub的政策。

**权限。** `storage`保存持仓、缓存与备份；`alarms`调度后台刷新；两个域名访问权限和 `declarativeNetRequestWithHostAccess` 用于获取行情及适配扩展自身请求的请求头。规则限定扩展ID作为请求发起方，不修改普通网页请求。不申请全网站、浏览历史或读取网页内容权限。

**保留和删除。** 本地数据在卸载前保留，用户可修改、删除或清空当前持仓；为便于恢复，旧记录可能仍在最多10份自动备份及行情缓存中。卸载将删除扩展本地数据。下载到电脑的CSV、备份以及外部已分享副本不随卸载删除，需自行管理。更新前请先导出CSV。

**反馈。** 请通过 https://github.com/power32m/fund-note/issues 提交不含敏感信息的问题说明。不要公开上传真实持仓、CSV、完整浏览器配置、凭据或付款信息。如需调整本说明，会更新此页面并注明日期。

## English

Scope: Fund Note Chrome extension 1.0 test build. Effective: 2026-10-30.

**Local data.** Fund codes/names, units, costs, caches, request times and up to ten pre-edit snapshots are stored in `chrome.storage.local`. There are no application accounts, cloud sync, author-operated analytics, advertising trackers, or webpage/browsing-history collection. Local storage is not an encrypted vault; someone with device/profile access may access the data.

**Network requests.** Quotes are requested only from `hq.sinajs.cn` and `fundmobapi.eastmoney.com`, with fund/index codes and fixed interface parameters, not holding units or costs. Providers may receive IP addresses, request times, client identifiers and ordinary connection metadata under their own policies. GitHub's policies also apply when users visit project pages or download files.

**Permissions.** `storage` saves portfolios, caches and snapshots; `alarms` schedules refreshes. Access to the two quote domains and `declarativeNetRequestWithHostAccess` enables quote fetching and request-header adaptation. Rules are restricted to this extension ID as initiator and do not modify normal webpage requests. No all-site, history or page-content access is requested.

**Retention and deletion.** Local data persists until uninstall. Users can edit, delete or clear current holdings; previous records may remain in up to ten local snapshots and quote caches. Uninstall removes extension-local data. Exported CSV, downloaded backups and externally shared copies must be managed separately and are not removed by uninstall. Export before updating.

**Feedback.** Use https://github.com/power32m/fund-note/issues without sensitive information. Do not post real holdings, CSV, entire browser profiles, credentials or payment details. Policy changes will be reflected here with an updated date.
