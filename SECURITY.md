# 下载与分享安全 / Download safety

官方仓库：https://github.com/power32m/fund-note 。当前下载包为Edge 1.1.2；商店提交不等于通过审核。

仅下载对应Release的“FundNote-Edge-1.1.2.zip”和SHA256SUMS.txt。解压后manifest.json直接位于安装目录内。GitHub自动生成的Source code包只含文档，不能安装。

在PowerShell运行 Get-FileHash -LiteralPath '.\FundNote-Edge-1.1.2.zip' -Algorithm SHA256 并与校验文件比较。校验只能发现文件差异，不能独立保证软件安全。核对名称、版本及仅新浪/东方财富两个行情域名权限。不需要管理员权限、账号密码或关闭安全软件。

首次为空持仓。不要分享个人浏览器配置、CSV或真实资产截图。更新前导出CSV；相同目录覆盖后重新加载，不要先卸载。浏览器或扩展ID变化可能需要CSV迁移。旧缓存可能保留在本地备份中；卸载不删除导出文件。

行情缺失不等于零收益，缺口连接不代表真实中间行情。反馈仅提供版本、步骤和脱敏截图。使用Issues前隐藏个人数据；安全漏洞不要公开可直接利用的细节。

## English

Download only the matching Edge 1.1.2 ZIP and SHA256SUMS.txt from the official release. GitHub Source code archives contain documentation, not the installable application. Verify SHA256, extension name/version and the two quote-host permissions; hashes do not independently guarantee safety. No administrator privileges or credentials are needed. Export CSV before updates; keep the same unpacked directory and reload. Different IDs/profiles may need CSV migration. Fresh installs are empty. Never share private profiles, CSV or real portfolio screenshots. Quote gaps and stale data require attention. Report issues with redacted details, not exploitable security information.
