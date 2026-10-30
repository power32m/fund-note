# 基金小笺隐私政策 / Fund Note Privacy Policy

适用范围：基金小笺浏览器扩展1.1.1；既有1.0版本未包含下述日内走势和打赏入口，其余共同数据处理说明仍适用。修订日期：2026-10-30。

Scope: Fund Note browser extension 1.1.1. Existing version 1.0 does not include the intraday charts or support QR feature described below; statements about shared data practices still apply. Revised: 2026-10-30.

## 中文

基金小笺用于本地记录基金持仓并展示第三方行情。无需软件账号；作者未设置用于接收持仓的服务器，不提供云端同步、广告追踪或使用统计，也不收集网页正文、浏览历史或账号密码。

**本地数据。**基金代码、名称、份额、成本、行情缓存、设置、最多10份修改前持仓快照和日内估值点保存在扩展的本地存储中。走势最多保留最近5个已采集行情日，并受容量上限约束，在加载或写入时清理。删除持仓会移除对应走势，清空持仓会清空走势。卸载扩展或清除其数据会删除本地记录；您自行导出的CSV及已保存的其他副本不会因此自动删除。CSV包含持仓信息，需自行保管。删除或清空当前持仓后，旧记录可能仍保留在最多10份自动备份和行情缓存中。本地存储不是加密保险箱，能访问设备或浏览器配置的人可能接触数据。

**行情访问。**扩展仅向 hq.sinajs.cn 与 fundmobapi.eastmoney.com 请求所需行情，发送基金/指数代码及接口固定参数，不发送您录入的份额和成本。第三方服务仍可能按其自身政策处理IP地址、请求时间、请求头等连接信息。作者无法控制第三方服务的可用性和处理方式。用户主动访问项目GitHub页面时，也适用GitHub的隐私政策。

**权限用途。**storage用于本地数据；alarms用于后台定时更新；两个站点的访问权限用于行情请求；declarativeNetRequestWithHostAccess用于针对扩展自身行情请求设置接口所需请求头，规则限定为扩展发起的指定站点请求，不修改普通网页请求。扩展不要求读取所有网站或浏览历史。

**自愿打赏。**扩展在本地显示作者提供的微信收款码，不自动发起付款，不接入支付结果查询，不读取或保存支付结果。只有您自愿使用外部支付平台时，相关支付信息才由该平台按其规则处理；请核对收款人并了解平台隐私条款。

**控制与反馈。**您可修改或删除持仓、导出CSV，或卸载并清除本地数据；公开反馈请勿上传持仓、账号、CSV及支付凭证。如需联系作者，请通过项目反馈入口：https://github.com/power32m/fund-note/issues 。后续若改变数据用途或权限，将同步更新政策及版本说明。本政策不排除法律规定的权利与责任。

## English

Fund Note records fund holdings locally and displays third-party quotes. No application account is required. The author operates no server for receiving holdings. The extension provides no cloud sync, advertising tracking or usage analytics and does not collect web-page content, browsing history or account passwords.

**Local data.** Fund codes, names, units, costs, quote caches, settings, up to ten pre-edit portfolio snapshots and intraday estimate points are stored locally by the extension. Charts retain up to five collected quote days, subject to a storage cap; cleanup runs on loading or writing. Removing a holding removes its chart; clearing holdings clears chart history. Uninstalling or clearing extension data removes local records, but does not automatically remove CSV files or other copies you saved outside the extension. Exported CSV files contain portfolio information and should be kept private. After current holdings are deleted or cleared, previous records may remain in up to ten snapshots and quote caches. Local storage is not an encrypted vault; someone with device or browser-profile access may access the data.

**Quote services.** Requests go only to hq.sinajs.cn and fundmobapi.eastmoney.com for required quotes. Requests include fund/index codes and fixed API parameters, not the units or costs you enter. Providers may process IP addresses, request times, headers and other connection metadata under their own policies. The author does not control these services or their availability. GitHub’s privacy policy also applies when you voluntarily visit the project’s GitHub pages.

**Permissions.** storage saves local data; alarms schedules background updates; host access is limited to the two quote domains. declarativeNetRequestWithHostAccess sets headers needed for the extension's own quote requests, scoped to the extension initiator and specified destinations. It does not change ordinary website requests. No access to all websites or browsing history is requested.

**Voluntary support.** A locally bundled WeChat payment QR code is displayed on request. The extension does not initiate payments, query payment status, or read/store payment results. If you voluntarily use an external payment platform, its policies apply. Verify the recipient and review the platform's privacy terms yourself.

**Your controls and contact.** You may edit/remove holdings, export CSV, or uninstall and clear local data. Do not post holdings, account details, CSV files or payment receipts in public feedback. Contact: https://github.com/power32m/fund-note/issues . Changes in data use or permissions will be reflected in the policy and release notes. Statutory rights and responsibilities are not excluded.
