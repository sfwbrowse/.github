# SFWbrowse

<p align="center">
  <strong>Lightweight, zero-telemetry multi-browser safe browsing enforcement</strong><br>
  Built for Google Chrome, Mozilla Firefox, and Apple Safari.
</p>

---

## Overview

**SFWbrowse** is a client-side safe browsing extension suite that protects users from unsolicited adult, explicit, and graphic content without relying on invasive external proxies, VPNs, or third-party DNS resolvers.

### Core Architecture & Repositories

The SFWbrowse ecosystem is organized into a modular monorepo architecture:

- **[sfwbrowse-core](https://github.com/sfwbrowse/sfwbrowse-core)**: Single source of truth containing shared business logic, rule catalogs (`rules/cookies.json`, `rules/blocklist.json`, `rules/safesearch-rules.json`), native test suites, and synchronization scripts.
- **[sfwbrowse-chrome](https://github.com/sfwbrowse/sfwbrowse-chrome)**: Manifest V3 distribution port for Chromium browsers (Google Chrome, Microsoft Edge, Brave, Opera).
- **[sfwbrowse-firefox](https://github.com/sfwbrowse/sfwbrowse-firefox)**: Manifest V3 distribution port for Mozilla Firefox (`sfwbrowse@faiz.at`).
- **[sfwbrowse-safari](https://github.com/sfwbrowse/sfwbrowse-safari)**: Safari Web Extension distribution port with macOS XcodeGen project specification.
- **[.github](https://github.com/sfwbrowse/.github)**: Organization profile, global workflows, and community templates.

---

## Key Capabilities

1. **Automated Cookies Mode**: Automatically sets and monitors safe browsing cookies across target search engines (Bing, DuckDuckGo, Qwant, Ecosia) and privacy frontends (RedditP, Teddit, Libreddit/Redlib, Invidious, ProxiTok).
2. **Client Storage Guard (SPAs)**: Injects an immutable `document_start` lock for Single Page Applications (e.g. Troddit) where adult filters reside in `window.localStorage`.
3. **Hardware-Accelerated DeclarativeNetRequest (DNR)**: Enforces network-level domain blocking and SafeSearch query parameter / HTTP header rewrites without per-request JavaScript execution latency.
4. **Zero-Telemetry Guarantee**: 100% offline-first. Zero tracking, zero remote configuration pings, zero telemetry beacons.

---

## License

MIT © [Faiz A](https://faiz.at)
