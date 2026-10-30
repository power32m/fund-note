# Illustrated Chrome guide

[Project overview](../README.en.md) · [简体中文](CHROME.zh-CN.md)

Version: Chrome 1.0 test build (1.0.0). Screenshots use fictional codes such as 990001 and synthetic prices. Do not enter these example codes as real holdings.

## 1. Install and pin

Download `FundNote-Chrome-1.0.0-test.zip` from the [release](https://github.com/power32m/fund-note/releases/tag/chrome-v1.0.0-test), verify its checksum and extract it. Open `chrome://extensions` → Developer mode → Load unpacked → select the **chrome-extension** directory, not the ZIP or its parent directory.

Pin Fund Note through Chrome's extensions menu. A fresh installation has no holdings. Chrome 127 or later is required. Keep the extracted directory in place.

## 2. Add holdings

Choose “添加持仓” (Add holding). Enter a six-digit fund code, units and cost per unit, then save. An unknown cost can be left blank: total holding return will be unavailable, while quote-day return can still be calculated from units when quotes are available. Not every fund has intraday estimates.

<img src="images/chrome-add.png" width="600" alt="Add-holding form with a fictional fund code">

## 3. Read the popup and toolbar badge

The large number is quote-day return; confirmed assets appear on the right. Each row shows that fund's daily return and percentage. Clicking outside closes the popup; click the icon to reopen it.

<img src="images/chrome-popup.png" width="600" alt="Popup showing a synthetic portfolio">

The original blue icon has a native badge: red background for profit, green for loss. White digits show the rounded absolute amount, without signs or decimals. Hover for the signed amount, quote date and update time. No available return means no numeric badge. For partial coverage, check the popup and tooltip.

Before today's quotes arrive, “最近行情日收益” means returns for the latest available quote day, with its date shown. Returns from different dates are never combined.

## 4. Expand indices and refresh

Hover over the bottom ticker for one second to expand a compact two-column panel. It fades out on pointer exit. Red means up and green means down; update flashes indicate a change from the previous fetched price.

<img src="images/chrome-markets.png" width="600" alt="Expanded index panel with synthetic prices">

Use the top-right refresh button or click the quote time. They share a ten-second cooldown. Confirmed NAV has its own cache/request interval, so repeated clicks may not fetch new figures.

## 5. Edit or delete in the detailed view

The top-right list button opens the detailed view in a new tab. Click “修改” (Edit) before changing units or cost, then “保存” (Save), or “取消” (Cancel). Enter saves; Esc cancels. Dragging a row left reveals actions; right-side buttons are also available. Delete and Clear ask for confirmation.

![Detailed portfolio view with fictional holdings](images/chrome-detail.png)

![Editing units and cost after choosing Edit](images/chrome-edit.png)

When multiple pages are open, a stale page cannot overwrite a newer saved portfolio. If a conflict message appears, reopen the page and check the latest values before editing.

## 6. Import, export and restore CSV

Choose “CSV与设置” (CSV & settings) at the bottom of the popup. Import/export is also available below the detailed table.

![CSV settings and local snapshots](images/chrome-settings.png)

- **Export:** download the current holdings as CSV with columns 基金代码 (code), 基金名称 (name), 份额 (units), 成本价 (cost per unit).
- **Import:** select a CSV, review the validated preview and confirm replacement. Invalid files do not overwrite holdings.
- **Restore:** download a snapshot from “最近的自动备份” (Recent automatic backups), then import that CSV. Up to ten pre-edit snapshots are kept.

UTF-8, UTF-16LE and common GB encodings are supported; exports use UTF-8 with BOM. Leading zeros are preserved, and extra quote columns from desktop CSV exports are ignored. CSV contains portfolio information: do not attach it to public issues or distribution packages.

## 7. Update, uninstall and migrate

Export a CSV first. Close extension pages, replace runtime files in the original installation directory, and click Reload at `chrome://extensions`. Updating the same unpacked directory preserves data; do not uninstall first. A future store build may have another ID and require CSV migration.

Uninstalling clears extension-local holdings and snapshots. Desktop and Chrome data are separate; transfer through CSV. Read [Privacy](../PRIVACY.md) and [Security](../SECURITY.md).
