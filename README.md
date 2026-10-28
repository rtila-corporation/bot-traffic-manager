<div align="center">

<img src="https://i.imgur.com/ZwTz5yP.gif" alt="Bot Traffic Manager" width="100%" />

# Bot Traffic Manager

**Stop AI Scrapers. Block Bad Bots. Take Back Your Bandwidth.**

[![WordPress](https://img.shields.io/badge/WordPress-6.5%2B-blue.svg?style=flat-square&logo=wordpress)](https://wordpress.org)
[![PHP](https://img.shields.io/badge/PHP-8.1%2B-purple.svg?style=flat-square&logo=php)](https://php.net)
[![Version](https://img.shields.io/badge/Version-2.5.4-orange.svg?style=flat-square)](https://github.com/rtila-corporation/bot-traffic-manager/releases)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

<br />

**A 100% self-hosted alternative to Cloudflare, DataDome, and other Cloud WAFs.** 
Bot Traffic Manager runs entirely inside your WordPress installation. No visitor data ever leaves your server.

<br />

<a href="https://github.com/rtila-corporation/bot-traffic-manager/releases/latest/download/bot-traffic-manager.zip">
  <img src="https://img.shields.io/badge/⬇_Download_Free_Version-1E1E1E?style=for-the-badge&logo=github&logoColor=white" alt="Download Free" height="45" />
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://rtila.com/bot-traffic-manager">
  <img src="https://img.shields.io/badge/🔑_Purchase_Pro_License-2271B1?style=for-the-badge&logo=wordpress&logoColor=white" alt="Buy Pro" height="45" />
</a>

<br />
<br />

</div>

---

## 🛑 The Problem: AI Scrapers are Killing Your Site

Every day, your WordPress site is hit by thousands of automated requests. 
* **AI Training Crawlers** (GPTBot, ClaudeBot, CCBot) are stealing your content for free.
* **SEO & Marketing Bots** are draining your server resources and slowing down your site.
* **Spam Bots** are hammering your login page and checkout forms.

Traditional solutions are flawed:
* **Cloud WAFs** (Cloudflare, DataDome) process your traffic on *their* servers, compromising privacy and costing hundreds of dollars a year.
* **Basic WordPress plugins** only block by User-Agent, which any smart scraper can easily spoof.

---

## ⚡ The Solution: Bot Traffic Manager

Bot Traffic Manager is a lightweight, deeply integrated WordPress plugin that intelligently classifies *every* request into **7 distinct categories**, allowing you to **Allow, Challenge, Throttle, or Block** them with a single click.

### 🧠 Smart 7-Way Classification
1. **Verified Search Engines** (Googlebot, Bingbot - checked against official IPs)
2. **Verified AI Search** (Perplexity, etc.)
3. **Verified AI Training** (GPTBot, ClaudeBot, CCBot)
4. **Verified AI Agents** (AI browsing on behalf of a user)
5. **Unverified** (Bots pretending to be someone else)
6. **Human** (Real, genuine visitors)
7. **Suspicious** (Browser-like traffic executing automated scripts)

### 🛡️ Key Features
* **🤖 Stop AI Content Scraping:** Block AI training bots and automatically publish standard `robots.txt` and `RSL` (Really Simple Licensing) opt-outs.
* **🔒 Protect WooCommerce:** Guard your cart, checkout, and my-account pages from automated brute-force attacks.
* **🚫 Stop Login Brute Force:** A smart Login Guard that challenges failed attempts (progressive delay) without permanently locking out real users who forgot their password.
* **🔐 WordPress Hardening:** One-click toggles to disable XML-RPC, block user enumeration, restrict anonymous REST API access, and lock down sensitive files (`.env`, `.git`).
* **⚡ Edge Handoff (Performance):** Generate Apache/Nginx rules to block bots at the server level before WordPress even boots, saving massive CPU.
* **🔏 Privacy by Design:** 100% self-hosted. The Proof-of-Work challenge and fingerprinting run *entirely on your own domain*. No third-party vendors.

---

## 💎 Observe Mode (Free) vs. Active Mode (Pro)

You can start using Bot Traffic Manager for **free today** in Observe Mode. It will silently record everything bots do on your site so you can see the damage before you block them.

| Feature | 🟢 Free (Observe Mode) | 🔵 Pro (Active Mode) |
| :--- | :---: | :---: |
| **Traffic Analytics Dashboard** | ✅ | ✅ |
| **Bot Classification (7-Way)** | ✅ | ✅ |
| **Alerts & Daily Digests** | ✅ | ✅ |
| **Active Blocking & Throttling** | ❌ | ✅ |
| **ALTCHA Proof-of-Work Challenge** | ❌ | ✅ |
| **WordPress Hardening Controls** | ❌ | ✅ |
| **AI Content Ledger & Bot Tax** | ❌ | ✅ |
| **Client-Side Verdict Gate** | ❌ | ✅ |
| **License** | Free Forever | [Purchase Pro](https://rtila.com/bot-traffic-manager) |

👉 **[Download the Free Version (ZIP)](https://github.com/rtila-corporation/bot-traffic-manager/releases/latest/download/bot-traffic-manager.zip)** | 👉 **[Upgrade to Pro](https://rtila.com/bot-traffic-manager)**

---

## 📸 Screenshots

<div align="center">

<img src="https://i.imgur.com/9qfeQuI.gif" width="800" />
<img src="https://i.imgur.com/rNm5mzL.gif" width="800" />
<img src="https://i.imgur.com/LeGvrvr.gif" width="800" />
<img src="https://i.imgur.com/G65X8ti.gif" width="800" />
<img src="https://i.imgur.com/QRs212z.gif" width="800" />
<img src="https://i.imgur.com/HXn5Vsz.gif" width="800" />
<img src="https://i.imgur.com/smDA52i.gif" width="800" />
<img src="https://i.imgur.com/JIM47eQ.gif" width="800" />

</div>

---

## 🚀 Installation

### Manual Installation (GitHub)
1. Click the green **Code** button at the top of this repository and select **Download ZIP**.
2. In your WordPress admin, go to **Plugins → Add New → Upload Plugin**.
3. Upload the `.zip` file you just downloaded and click **Install Now**.
4. Activate the plugin.
5. Navigate to **Bot Traffic → Settings** to configure your preferences.

### WP-CLI Installation (Developers)
```bash
wp plugin install https://github.com/rtila-corporation/bot-traffic-manager/releases/latest/download/bot-traffic-manager.zip --activate
```

---

## 🛠️ Technical Architecture

Built for high-traffic enterprise environments.
* **L0 (auto_prepend_file):** Blocks traffic before WordPress even boots.
* **L2 (mu-plugin):** Blocks traffic before standard plugins load.
* **L3 (plugins_loaded):** The authoritative enforcement layer.
* **Atomic Storage:** Uses custom database tables, object cache, or highly optimized flat files to prevent database locking under bot floods.

<div align="center">
<br />
<a href="https://rtila.com"><img src="https://img.shields.io/badge/Built_with_❤️_by_RTILA_CORPORATION-black.svg?style=flat-square" alt="RTILA Corporation" /></a>
</div>
