# Fund Note · 基金小笺

[简体中文](README.md) · [Download 1.0 test build](https://github.com/power32m/fund-note/releases/tag/chrome-v1.0.0-test) · [Illustrated guide](docs/CHROME.en.md) · [Privacy](PRIVACY.md)

**A compact Chrome popup for fund holdings and indicative returns for the latest available quote day.**

Fund Note is an independently developed Chrome extension with a popup, a detailed portfolio view and CSV import/export. Holdings stay in local browser storage; no application account is required.

Current version: **Chrome 1.0 test build (1.0.0)**. The UI is in Chinese, with Chinese and English documentation. It is **not listed in the Chrome Web Store**; this build is loaded in developer mode.

This repository hosts documentation, screenshots and release downloads. **The application is proprietary, and its source is not published here.** Installed extension resources can be inspected; that does not grant an open-source license.

> Quotes and estimates are for reference only, not investment advice. Fund managers' and trading platforms' confirmed information takes precedence. Third-party services may be delayed, interrupted or discontinued. No real-time availability, long-term availability or ongoing maintenance is promised. Read the [disclaimer](DISCLAIMER.en.md) and [download safety notes](SECURITY.md).

## Preview

These are captures of the extension pages using fictional funds and synthetic fund/index prices. They do not show anyone's actual holdings or investment performance.

<img src="docs/images/chrome-popup.png" width="600" alt="Popup with a synthetic portfolio, quote-day returns and confirmed assets">

![Detailed view with synthetic units, costs, NAVs and holding returns](docs/images/chrome-detail.png)

## Features

- **Compact popup:** quote-day total return, per-fund daily return and percentage, with confirmed assets shown separately. Space for three funds by default; larger portfolios grow and then scroll.
- **Native toolbar badge:** the original icon stays visible. A red background means profit; green means loss. White digits show the rounded absolute amount. Hover for the signed amount, quote date and update time. The badge and popup share the same calculations.
- **Detailed portfolio view:** inspect units, cost per unit, confirmed and estimated NAV, and holding returns. Choose “修改” (Edit) before changing values, then save or cancel.
- **Index ticker:** a single scrolling row expands into a compact two-column panel after a one-second hover and fades out when the pointer leaves.
- **CSV and backups:** imports are validated and previewed before replacement. Up to ten pre-edit snapshots are stored locally and can be downloaded as CSV.
- **Controlled refresh:** market-session scheduling, shared caches, request deduplication and manual refresh cooldowns.

## Download and install

1. Open the [Chrome 1.0 test release](https://github.com/power32m/fund-note/releases/tag/chrome-v1.0.0-test). Download **FundNote-Chrome-1.0.0-test.zip** and **SHA256SUMS.txt**.
2. [Verify the SHA256](SECURITY.md), extract the ZIP, and keep the extracted directory in place.
3. In **Chrome 127 or later**, open `chrome://extensions` and enable Developer mode.
4. Choose “Load unpacked” and select the extracted **chrome-extension** directory.
5. Pin Fund Note from Chrome's extensions menu, open it, and enter your own fund codes, units and cost per unit.

A fresh installation has no holdings. To update an existing unpacked installation, replace the runtime files in the same directory and click Reload; **do not uninstall first**. A future store build may have a different extension ID, so export CSV before migration.

GitHub's automatic **Source code (zip/tar.gz)** archives contain only this documentation repository and are not installable extension packages. See the [illustrated guide](docs/CHROME.en.md).

## Return calculations and refresh

Quote-day return and total holding return are different measures. Daily return is estimated from units and the day's NAV change; confirmed assets and holding returns use the latest confirmed NAV. Intraday estimates may differ from final figures. Cost precision, dividends, fees, FX and platform methods may also produce differences. The extension does not maintain full transaction/dividend/fee records or execute trades.

Before today's quotes arrive, the popup explicitly shows returns for the latest available quote day. It switches back when today's data arrives and never combines returns from different dates. Missing data is indicated. The badge omits signs and decimals; hover or open the popup for the signed amount. Long amounts are limited by Chrome's badge space.

During active sessions, visible pages typically attempt refreshes every 15 seconds and the background every 60 seconds; intervals increase outside sessions. Manual estimate/index refreshes have a 10-second cooldown. Confirmed NAV normally has a five-minute cache and at least a 60-second manual interval. These are request intervals, not provider update guarantees. Browser sleep, shutdown and networking can delay updates. The exchange calendar covers 2026, with weekday/session fallback in later years.

## Privacy, support and license

Holdings, caches and snapshots use `chrome.storage.local`. There is no author-operated account, portfolio-sync, advertising or telemetry service. Quote requests send fund/index codes, not units or costs; providers can still receive IP addresses and ordinary connection metadata. CSV files contain holdings: do not attach them to public issues. Uninstalling removes local extension data; export first. See [Privacy](PRIVACY.md).

Report issues through [GitHub Issues](https://github.com/power32m/fund-note/issues), including extension/Chrome versions, reproduction steps and redacted screenshots. See [Security](SECURITY.md) for sensitive reports. Chrome and desktop data are separate. This extension contains no payment QR code, Windows tray, desktop pinning or startup integration.

Author: 无痛穿耳 / power32m. See the [proprietary distribution notice](LICENSE), [third-party notices](THIRD_PARTY_NOTICES.md) and [changelog](CHANGELOG.md).
