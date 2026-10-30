# 下载与分享安全 / Download and sharing safety

## 中文

- 官方仓库：https://github.com/power32m/fund-note 。本次发布为Chrome扩展测试版，尚未在Chrome Web Store上架。
- 仅下载Release中的 `FundNote-Chrome-1.0.0-test.zip`。自动生成的Source code压缩包只有文档，不能安装。不要安装来源不明的改包，也不需要管理员权限或浏览器账号密码。
- 同时下载 `SHA256SUMS.txt`，在PowerShell运行下面命令，将结果与校验文件比较。校验能发现文件差异，不能单独证明软件安全；若下载来源或作者账号受损，单靠校验不够。

```powershell
Get-FileHash -LiteralPath '.\FundNote-Chrome-1.0.0-test.zip' -Algorithm SHA256
```

- 加载扩展前核对：扩展名“基金小笺”、版本1.0.0；网络权限仅涉及 `hq.sinajs.cn` 和 `fundmobapi.eastmoney.com`。不要求全网站访问、账号凭据或关闭安全软件。
- 分发包首次安装为空持仓，不含作者个人数据。分享官方Release链接或未修改的原ZIP；不要把自己浏览器里的数据、CSV、自动备份或截图中的真实资产一起打包。
- 更新前导出CSV；已有解压安装保持原目录并点击“重新加载”。不要为更新先卸载，以免删除本地持仓。未来商店版可能需要CSV迁移。
- 行情取数失败时保留旧数据，注意日期和更新时间。旧行情、部分行情和盘中估值不能作为确认收益。
- 反馈时仅提供版本、操作步骤及脱敏截图。普通问题使用Issues；安全问题若没有私密报告入口，请先公开描述不含细节的问题类别以联系作者，不要公开凭据、个人持仓或可被直接利用的细节。

## English

The official repository is https://github.com/power32m/fund-note . This is a Chrome test build, not a Chrome Web Store listing.

Download `FundNote-Chrome-1.0.0-test.zip` and `SHA256SUMS.txt` from its Release. Automatic Source code archives contain documentation only. Avoid modified/repacked downloads. No administrator privileges, account credentials or disabled security software are required.

Use the PowerShell command above to compare the ZIP's SHA256 with the checksum file. A match detects file differences, but is not an independent security certification, especially if a download source or publisher account is compromised.

Check the name “基金小笺”, version 1.0.0, and quote access limited to `hq.sinajs.cn` and `fundmobapi.eastmoney.com`. No all-site or credential access is required. Share the official release link or original ZIP, not browser data, holdings CSV or unredacted screenshots. Fresh installations contain no holdings.

Export before updating; replace files in the same directory and Reload rather than uninstalling. A future store build may require CSV migration. Check quote dates after errors; cached, partial or estimated data is not a confirmed return.

Report versions, reproduction steps and redacted screenshots through Issues. If no private security-reporting channel is available, first contact the author with a non-sensitive issue category. Do not publicly disclose credentials, portfolios or directly exploitable details.
