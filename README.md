Take control of your bot traffic. See who is visiting, block the ones you don't want, keep the search engines, and stop paying for AI scrapers to copy your content.

# Description

Every day, bots visit your site. Some are helpful (Google, Bing). Many are harmless (social previews, uptime monitors). A growing number are not: AI companies training their models on your writing, scrapers copying your product pages, spam bots hammering your login form, and automated traffic that burns through your hosting quota without ever buying anything.

Bot Traffic Manager shows you exactly what all of that traffic is doing, and gives you one simple decision for each kind: **Allow it, Challenge it, Throttle it, or Block it.** You can start in Observe mode (record everything, block nothing), watch what actually happens for a few days, then flip to Active mode when you are ready.

## Who is this for?

* **Bloggers and publishers** — stop AI companies from training their models on your content for free.
* **Store owners** — protect cart, checkout, and account pages from automated abuse.
* **Agencies** — deploy a single configuration across client sites and manage license seats from one place.
* **Anyone on shared hosting** — find out why your site is slow, and cut the traffic that is doing the damage.
* **Site owners who just want the spam to stop** — turn on Active mode and let the defaults handle it.

## How does it work?

Bot Traffic Manager sorts every visitor into one of seven groups:

* **Verified search engines** — Google, Bing, Apple. Checked against their published IP addresses, so a spoofer cannot pretend to be Googlebot.
* **Verified AI search** — Perplexity and similar, verified the same way.
* **Verified AI training** — GPTBot, ClaudeBot, Common Crawl, and others, verified the same way.
* **Verified AI agents** — AI tools browsing on behalf of a real person.
* **Unverified** — anything that claims to be a known bot but could not be proven, plus unrecognised automated traffic.
* **Human** — real visitors using a real browser.
* **Suspicious** — browser-like traffic that looks automated.

For each group, you pick one action:

* **Allow** — let it through.
* **Challenge** — show a quick "prove you're human" puzzle. Real visitors solve it once and are remembered for hours. Bots almost never can.
* **Throttle** — slow it down so it can't hog your server.
* **Block** — refuse it entirely.

That's the whole model. No rules to write, no regex, no API keys. The defaults are sensible and you can change them with a dropdown on the Policies screen.

## Observe first, enforce later

Turning on Active mode on day one is scary. So we start you in **Observe mode**: the plugin watches every bot, records what it did, and shows you the numbers — but does not block anything.

After a day or two you will see real data on the dashboard:

* "GPTBot read 1,240 of your pages yesterday."
* "Bytespider tried to scrape your shop 3,200 times."
* "47 login attempts from 12 countries at 3 a.m."

Then you click one button. Now those bots are blocked, challenged, or throttled — your choice, per group. No configuration change you didn't explicitly ask for.

## What you can do once Active mode is on

* **Stop AI training crawlers** — block GPTBot, ClaudeBot, CCBot, Google-Extended, Applebot-Extended, and the rest. Also publishes the industry-standard **RSL** licensing file and updates your `robots.txt` so the AI companies see your choice.
* **Protect your login page** — the login guard tracks failed attempts and escalates politely: challenge first, slow down next, temporary lockout last. A real user with a typo gets a brief pause, never a permanent lockout.
* **Block automated form spam** — hidden-field honeypots on comments, registration, lost-password, and WooCommerce checkout. No CAPTCHA for real visitors.
* **Close WordPress attack surfaces** — turn off XML-RPC, stop strangers from listing your usernames, lock down the REST API for anonymous callers, block direct requests to sensitive files like `.env` and `.git`, and stop external services from triggering your background jobs.
* **Block Tor exit nodes** — one switch if you don't want anonymous-network traffic.
* **Throw up an emergency shield** — one click blocks all unverified, AI-training, and suspicious traffic immediately, then restores your normal policies the moment you turn it off.
* **Get a server-level speed boost** — the Edge Handoff Wizard writes Apache or Nginx rules that refuse blocked bots before they even reach WordPress. On a busy site this can be a meaningful CPU saving.
* **Export reports and invoices** — download a CSV or PDF of your bot traffic, or generate a "Bot Tax" invoice that shows what your hosting bill would have been without the plugin.
* **See what AI consumed** — the AI Content Ledger estimates how many gigabytes of your content AI crawlers have read, in plain numbers.
* **Publish a transparency page** — a single HTML page stating exactly how your site treats AI crawlers, ready to host anywhere.

## Privacy by design

* **Nothing about your visitors leaves your site.** No third-party analytics, no external challenge service, no fingerprint vendor. The challenge runs on your own server.
* **IP addresses are anonymized by default.** The last octet of every address is removed before any record is written.
* **You can turn off any data collection.** Fingerprint scoring, behavioural telemetry, and page-view proof are all disabled by default. Turn them on only if you want them, and hook in your own consent-management tool if your jurisdiction requires it.
* **No tracking cookies for real visitors.** The challenge cookie is used only to remember that a visitor solved a challenge, and is deleted when it expires.

## Works with your existing setup

* **Caching plugins** — WP Rocket, WP Super Cache, W3 Total Cache, LiteSpeed Cache, Cloudflare APO, Kinsta, WP Engine, SiteGround, and most others are detected automatically. The plugin tells you exactly what each one does and does not allow it to enforce on cached pages, so you are never lied to about what is protected.
* **WooCommerce** — cart, checkout, and account pages get extra protection. Payment-processor webhooks are always exempt.
* **Shared hosting** — the plugin needs no special server access to work. Optional speed layers light up automatically if your host supports them.
* **Multisite** — not supported by design. The plugin is single-site only.

## What is free, and what is Pro?

**Observe mode is free forever.** The dashboard, the traffic charts, the per-class policies, and the alerts all work without a license. You can watch your traffic, learn what it looks like, and decide whether the paid version is worth it.

**Active mode — actually blocking, challenging, and throttling bots — requires a license.** So do the WordPress Hardening controls, the AI Content Ledger, the Bot Tax invoice, the transparency scorecard, and the cache-aware client-side protections.

Three plans:

* **Solo** — one site, full Active mode, full dashboard. Ideal for a personal site or blog.
* **Pro** — up to seven sites, shared settings, and the client-gate protections that work on fully cached pages.
* **Agency** — unlimited sites, unlimited shared license keys you can hand to clients under your own label.

## About the "Bot Tax"

The dashboard shows a dollar figure next to your bot traffic. It answers a simple question: *"If I paid for this bot traffic at my hosting rate, what would it cost me?"* The default rate is a rough guess; you can enter the real figure under Settings → Traffic. The invoice export turns that number into a document you can hand to your finance team or your client.

The estimate is honest about what it is: a rough gauge for decision-making, not a billing statement. Every input is labelled in the settings screen.

## Ready to start?

1. Install and activate the plugin.
2. Walk through the short setup wizard (about two minutes).
3. Leave it in Observe mode for a day or two.
4. Open the Dashboard and look at what your site is actually doing.
5. Enter a license key when you are ready to start blocking.

# Installation

1. In your WordPress admin, go to **Plugins → Add New**.
2. Search for **Bot Traffic Manager**.
3. Click **Install Now**, then **Activate**.
4. Follow the setup wizard that appears automatically.
5. (Optional) Enter your license key under **Bot Traffic → Licensing** when you are ready to switch from Observe mode to Active mode.

That's it. No configuration file edits. No server access required. No API keys to paste.

If you installed the plugin manually (uploading a ZIP file), the same steps apply once the plugin is activated.

# Frequently Asked Questions

## Do I need to know any code?

No. Everything is configured through the WordPress admin screens. The Edge Handoff Wizard (which generates optional server rules for advanced users) copies the snippet to your clipboard for you, but you don't have to use it.

## Will this break my site? Will it hurt my SEO?

Search engines like Googlebot and Bingbot are in their own group ("Verified search engines"), and the default policy for that group is **Allow**. Nothing in the default configuration will slow down, throttle, or block a real search engine crawl. You would have to explicitly change that group's policy to do it, and the plugin warns you twice before letting you.

## What is Observe mode? What is Active mode?

**Observe mode** records everything but blocks nothing. It's the "security camera" mode — useful for understanding your traffic before you change anything.

**Active mode** enforces the policies you have configured. It's the "security guard" mode — the plugin actually blocks, challenges, throttles, or allows each visitor based on the group they belong to.

You can switch between the two at any time from the Settings screen. Observe mode requires no license. Active mode requires a license.

## What do the four actions (Allow / Challenge / Throttle / Block) actually do?

* **Allow** — let the visitor through unchanged.
* **Challenge** — show a small "please verify you are human" puzzle. Real visitors solve it once and are remembered for hours. Automated tools usually cannot solve it at all.
* **Throttle** — let the visitor through, but rate-limit how fast. Useful for bots you don't want to fully block (e.g. SEO crawlers you want to slow but not stop).
* **Block** — refuse the visitor. They see an "access denied" page.

## Can I block AI training crawlers like GPTBot and ClaudeBot?

Yes. The **Verified AI training** group contains GPTBot (OpenAI), ClaudeBot (Anthropic), CCBot (Common Crawl), Bytespider (ByteDance), and most other large AI training crawlers. Its default policy is Block in Active mode.

The plugin also writes a `Google-Extended` and `Applebot-Extended` opt-out into your `robots.txt` — the two channels Google and Apple use to let publishers refuse AI training without affecting search.

## What is RSL and why should I care?

**RSL** (Really Simple Licensing) is a machine-readable file that tells AI companies exactly what your site permits. It is published at a well-known URL that crawlers can read. If you have ever wished there was a way to say "you may read this for search but not for training" in a format that a crawler actually understands, RSL is that.

The plugin generates one for you automatically from your policy settings. Turn it on under Settings → Traffic → Content Licensing.

## Does this work with my caching plugin?

Yes, and the plugin tells you honestly what each cache allows. Some caching setups (a full-page CDN like Cloudflare APO) mean cached pages are never seen by WordPress at all, so no server-side rule can block a bot on those pages. The plugin explains that clearly on the Settings screen and offers a client-side fallback (the "client-side verdict gate") for Pro customers.

There is no scenario where the plugin silently fails to protect a cached page and tells you it did.

## Does the challenge block real visitors?

No. The challenge is a small proof-of-work puzzle — the browser does a tiny amount of calculation, usually under a second, then the visitor is remembered for hours. Real visitors barely notice. If a real visitor does see one, it is because they were in a class you set to Challenge on purpose (e.g. "Suspicious" traffic), and their browser will solve it automatically.

The challenge also fails open: if the challenge service is temporarily unavailable, the visitor is let through rather than shown an error.

## Does this send my data to a third party?

No. Every visitor-related decision happens on your own server. The license key and update checks contact the plugin author's own service — never a visitor's data. The challenge puzzle runs on your own server. The AI detection, the traffic charts, the dashboards: all local.

IP addresses are anonymized by default (last octet removed). You can turn off every piece of client-side collection under Settings → Detection if you want the plugin to use only server-side signals.

## What is the difference between free and Pro?

The free version gives you **Observe mode** — the full dashboard, the traffic charts, the per-class policies, and the alerts. You can watch exactly what is happening on your site.

The Pro version adds **Active mode** — actually blocking, challenging, throttling, or allowing traffic according to your policies. It also unlocks the WordPress Hardening controls, the AI Content Ledger, the Bot Tax invoice, the transparency scorecard, and the cache-aware client-side protections.

If you just want to see what is hitting your site, the free version is enough. If you want to do something about it, you need a license.

## What happens if I uninstall the plugin?

By default, your settings and traffic history are preserved, so a reinstall picks up where you left off. A checkbox under Settings → Uninstall lets you remove everything permanently.

Regardless of that checkbox, the plugin cleans up its own files and stops all background jobs on uninstall — you will not find orphaned files or leftover scheduled events after removal.

## Does it work on shared hosting?

Yes. The plugin runs entirely inside WordPress and needs no special server access to work. If your host supports optional faster layers, the plugin will turn them on automatically. If not, it still works — just marginally slower under heavy bot pressure.

## Will it interfere with other plugins?

No. Bot Traffic Manager detects the most common cache, security, and WooCommerce plugins and works alongside them. If a specific integration has a limitation, the plugin tells you on the relevant settings screen instead of failing silently.

## I have a question that is not here.

Visit the support forum on WordPress.org, or contact us from the plugin's Help screen. We read every message.

# Screenshots

1. The main dashboard, showing bot traffic over time, top bots by server time, and the estimated cost of bot traffic ("Bot Tax").
2. The Policies screen, where you pick Allow / Challenge / Throttle / Block for each of the seven traffic groups.
3. The Bot Activity screen, with per-bot details — request counts, effective policy, first/last seen.
4. The Detection settings, where the risk thresholds and the self-hosted challenge are tuned.
5. The WordPress Hardening screen, with the toggles for the login guard, XML-RPC, user enumeration, and file access controls.
6. The AI Content Ledger, showing how many gigabytes of content AI crawlers have read and what your `robots.txt` says about it.

# Changelog

## 2.5.3
Initial public release.

This release brings the full feature set together in one plugin:

* A complete WordPress dashboard showing bot traffic, human traffic, top bots by server time, policy distribution, and a running "Bot Tax" estimate.
* Seven-way traffic classification — verified search, verified AI search, verified AI training, verified AI agents, unverified, human, and suspicious.
* Per-group policies: Allow, Challenge, Throttle, Block.
* Observe mode for learning your traffic, Active mode for enforcing policies.
* A self-hosted, privacy-friendly challenge with no third-party service.
* Detection of the most common page-cache setups, with honest reporting of what each one does and does not allow.
* The Edge Handoff Wizard, which generates Apache or Nginx rules that refuse blocked bots before they reach WordPress.
* WordPress Hardening controls: login guard, XML-RPC lockdown, user enumeration protection, REST API lockdown for anonymous callers, form honeypots, file editor and Application Passwords controls, sensitive file block, and external wp-cron block.
* The PHP2Shell probe shield (in response to the October 2026 critical PHP vulnerabilities).
* RSL publication and `robots.txt` AI-training opt-out.
* CSV and PDF report export, plus a PDF Bot Tax invoice.
* A one-click transparency scorecard you can host publicly.
* Full licensing with Solo, Pro, and Agency plans, and shared license keys you can hand to clients under your own label.

If you are upgrading from an earlier internal build, this is a substantial update — please read the release notes on the plugin homepage before activating Active mode.

# Upgrade Notice

## 2.5.3
Initial public release. See the Description section for the full feature list and the Getting Started guide.
