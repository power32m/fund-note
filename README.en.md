# Fund Note · 基金小笺

[简体中文](README.md) · [Download 1.1.2](https://github.com/power32m/fund-note/releases/tag/edge-v1.1.2) · [Illustrated guide](docs/CHROME.en.md) · [Privacy](PRIVACY.md)

A compact popup for fund holdings, quote-day returns and locally collected intraday estimates.

Current package: **Edge 1.1.2**. The UI is Chinese; store materials and documentation are bilingual. Tested in an isolated Edge 156 environment. An earlier submission entered Edge review; current store review/publication status must be checked in Partner Center. This GitHub download does not imply store approval. Not listed in the Chrome Web Store.

This repository contains documentation, demo screenshots and release packages, not application source code. The application is proprietary; installed extension resources are inspectable, without granting an open-source license.

## Preview

Screenshots use fictional holdings and market data, not actual investment results.

<img src="docs/images/01-popup.png" width="600" alt="Demo holdings and shared-scale charts">

![Detailed portfolio](docs/images/03-detail.png)

## Features

- Popup quote-day returns and assets, plus full-view units/cost management.
- Native integer badge: red background for gains, green for losses, white digits. Hover for signed amount and date.
- At most one valid estimate point per minute. Holdings for the same date share a zero-centered scale, starting at ±1% and expanding without shrinking that day, including after restart. Different dates have separate scales.
- Lunch break compressed. Effective trading-time intervals up to ten minutes connect with a solid line; longer gaps stay blank. Gap tooltips disclose missing data without inferred percentages. No synthetic points are stored.
- One-second hover index panel, CSV validation/preview before replacement, and up to ten local pre-edit snapshots.
- Session-aware refresh. Background wake-ups reuse the alarm; automatic one-minute polling allows five seconds of timing tolerance. Manual cooldowns remain strict.
- Optional WeChat support QR display, with no payment initiation or payment-result access. No payment unlocks features.

## Install and update

Download 基金小笺-Edge-1.1.2.zip and SHA256SUMS.txt from the [Release](https://github.com/power32m/fund-note/releases/tag/edge-v1.1.2). Verify the hash, extract, open edge://extensions, enable developer mode and choose Load unpacked. Select the folder directly containing manifest.json. Fresh installs are empty and need no application account.

Export CSV before updating. For an existing unpacked installation, retain the directory, replace runtime files and reload; do not uninstall first. A different extension ID, browser or profile may require CSV migration. Automatic GitHub Source code archives contain documentation only and cannot be installed. The 1.0 package remains historical.

## Limits and privacy

Indicative values may differ from confirmed fund/platform records. Latest-valid-day returns are dated, and different dates are not mixed. No comprehensive transaction/dividend/fee ledger, trading or investment recommendations are provided.

Charts begin with received data, keep up to five collected days subject to a storage cap, and do not backfill history. Solid connectors across short gaps do not represent observed intermediate quotes. Sleep, shutdown, network failures and unavailable estimates can leave gaps. Foreground active-session polling is typically 15 seconds; background checks are typically one minute. Polling does not guarantee source updates, real-time accuracy, continuous availability or ongoing maintenance.

Holdings, costs, charts and backups remain local, with no cloud sync, analytics or advertising tracking. Quote requests send codes and necessary parameters, not entered units or costs; providers may receive connection metadata such as IP addresses. Uninstalling clears local data; keep exported CSV private.

[Privacy](PRIVACY.md) · [Disclaimer](DISCLAIMER.en.md) · [Download safety](SECURITY.md) · [License](LICENSE) · [Third-party notices](THIRD_PARTY_NOTICES.md) · [Changelog](CHANGELOG.md)

[Feedback](https://github.com/power32m/fund-note/issues): do not post holdings, account or payment information. Author: 无痛穿耳 / power32m.
