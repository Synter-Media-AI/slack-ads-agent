# Slack Ads MCP Starter Kit — Get Ad Performance Alerts in Slack

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Slack](https://img.shields.io/badge/Platform-Slack-4A154B)](https://slack.com)

**Catch underperforming campaigns before they waste your budget.** Open this repo in Amp, Cursor, or VS Code and set up AI-powered Slack alerts for your ad campaigns — daily summaries, ROAS threshold warnings, budget pacing alerts, and anomaly detection delivered to your team's Slack channels.

---

## Why Slack for Ad Monitoring?

Marketing teams live in Slack. They don't live in Google Ads dashboards. By the time someone logs into each ad platform, checks performance, and notices a problem, hours or days of budget have been wasted.

Slack alerts flip the workflow. Instead of "check the dashboard," the dashboard comes to you. A campaign drops below 2x ROAS? You get a Slack message in 60 seconds. Budget pacing ahead by 30%? Alert. Creative CTR drops 50%? Alert. No more surprises at the Monday meeting.

An AI agent sets up these alerts, generates daily summaries, and answers ad-hoc questions — all without leaving Slack.

**Best for:** Teams who live in Slack, performance marketers monitoring multiple campaigns, agencies managing client budgets, anyone who wants proactive alerts instead of reactive dashboard checking.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **Daily Summary** | "Send a daily cross-platform performance summary to #marketing at 9 AM" |
| **ROAS Alerts** | "Alert me in Slack if any campaign ROAS drops below 2x" |
| **Budget Pacing** | "Warn me if any campaign is pacing to overspend by more than 20%" |
| **Anomaly Detection** | "Notify me about any unusual spend or performance changes" |
| **Campaign Status** | "Post to #ads when any campaign is paused or runs out of budget" |
| **Creative Fatigue** | "Alert when any ad creative's CTR drops below 50% of its peak" |
| **Weekly Report** | "Send a weekly executive summary every Monday at 8 AM" |
| **Threshold Alerts** | "Notify me when total spend exceeds $500/day across all platforms" |
| **Competitor Alerts** | "Alert when competitors start bidding on our brand keywords" |
| **New Campaign Notifications** | "Post to #ads when any new campaign goes live" |

---

## Example Conversations

### 1. Setting Up a Daily Morning Report

> **You:** I want a daily summary of all ad performance in #marketing-ads at 9 AM ET.
>
> **Agent:** I'll configure a daily cross-platform summary. Here's the report format:
>
> **📊 Daily Ad Performance — March 22, 2026**
>
> | Platform | Spend | ROAS | CPA | Conv. | vs Yesterday |
> |---|---|---|---|---|---|
> | Google Ads | $580 | 4.2x | $28 | 21 | ↑ 12% |
> | Meta Ads | $420 | 3.8x | $22 | 19 | ↓ 5% |
> | LinkedIn | $280 | 1.9x | $82 | 3 | → flat |
> | TikTok | $150 | 2.8x | $15 | 10 | ↑ 22% |
> | **Total** | **$1,430** | **3.5x** | **$27** | **53** | ↑ 8% |
>
> 🏆 **Top performer:** TikTok (2.8x ROAS, up 22%)
> ⚠️ **Watch:** LinkedIn ROAS declining 3 days in a row
>
> **Customization options:**
> - Platforms to include
> - Metrics to show (ROAS, CPA, CTR, spend, conversions)
> - Comparison period (vs yesterday, vs last week, vs last month)
> - Channel (#marketing-ads, #growth, DM, etc.)
> - Time zone and delivery time
>
> **You:** Perfect. Include all 4 platforms, compare vs yesterday, deliver at 8:30 AM ET to #growth.
>
> **Agent:** Configured. First report delivers tomorrow at 8:30 AM ET to #growth. It will include Google, Meta, LinkedIn, and TikTok with day-over-day comparison.

### 2. ROAS Threshold Alerts

> **You:** I need to know immediately when a campaign is losing money. Alert me if ROAS drops below 1.5x.
>
> **Agent:** Setting up real-time ROAS monitoring. Here's the alert configuration:
>
> **Alert: "ROAS Below Threshold"**
> - Trigger: Any campaign ROAS drops below 1.5x over a rolling 24-hour period
> - Channel: #ads-alerts
> - Mention: @you (direct mention for urgency)
>
> **Sample alert:**
>
> > 🚨 **ROAS Alert — Campaign Below 1.5x**
> > 
> > **Campaign:** Google Ads — "Competitor Keywords"
> > **Current ROAS:** 1.2x (threshold: 1.5x)
> > **Spend today:** $340
> > **Revenue today:** $408
> > **Trend:** Declining for 3 consecutive days
> > 
> > **Recommended actions:**
> > - Pause high-CPC keywords with 0 conversions
> > - Check search terms for irrelevant traffic
> > - Review landing page for issues
> >
> > Reply "pause" to pause this campaign immediately.
>
> **Alert tiers I recommend:**
> | Tier | Threshold | Action |
> |---|---|---|
> | ⚠️ Warning | ROAS < 2.0x | Monitor closely |
> | 🚨 Alert | ROAS < 1.5x | Investigate immediately |
> | 🔴 Critical | ROAS < 1.0x (losing money) | Pause campaign |
>
> Want me to set up all three tiers?

### 3. Budget Pacing and Overspend Prevention

> **You:** Last month we overspent our Google Ads budget by $2,000. How do I prevent that?
>
> **Agent:** I'll set up budget pacing alerts that catch overspending early. Here's the system:
>
> **Monthly budget: $10,000 for Google Ads**
>
> **Pacing alerts:**
>
> | Alert | Trigger | When |
> |---|---|---|
> | On Track ✅ | Daily spend within ±10% of $333/day | No alert (all good) |
> | Pacing Hot ⚠️ | On track to spend $11,000+ by month end | Alert on day 7, 14, 21 |
> | Overspend Risk 🚨 | On track to spend $12,000+ (20% over) | Alert immediately |
> | Budget Exhausted 🔴 | Monthly spend hits $10,000 | Alert + recommend pause |
>
> **Sample pacing alert:**
>
> > ⚠️ **Budget Pacing Alert — Google Ads**
> >
> > **Monthly budget:** $10,000
> > **Spent so far:** $5,200 (day 12 of 31)
> > **Projected monthly spend:** $13,417
> > **Over budget by:** $3,417 (34%)
> >
> > **Why:** Campaign "Product — Features" increased spend 40% this week due to a competitor pulling back (more impression share available at lower CPCs).
> >
> > **Options:**
> > 1. Reduce daily budget from $180 to $130
> > 2. Accept the overspend (lower CPCs = better efficiency)
> > 3. Pause the lowest-ROAS campaign to compensate
>
> This would have caught last month's overspend by day 10 instead of day 31.

### 4. Creative Fatigue Monitoring

> **You:** Can you alert me when ad creative starts dying?
>
> **Agent:** Yes — creative fatigue detection. I'll monitor CTR trends for every active creative and alert when performance declines:
>
> **Alert: "Creative Fatigue Detected"**
> - Trigger: Any creative's CTR drops to 50% of its peak CTR (measured over first 7 days)
> - Check frequency: Daily
> - Channel: #creative-alerts
>
> **Sample alert:**
>
> > 📉 **Creative Fatigue — Meta Ads**
> >
> > **Ad:** "Summer Collection — Hero Image"
> > **Peak CTR (week 1):** 2.4%
> > **Current CTR (week 4):** 1.1% (54% decline)
> > **Frequency:** 4.8 (avg person has seen this ad 4.8 times)
> > **CPA impact:** $22 → $38 (+73%)
> >
> > **This creative is burned out.** Frequency of 4.8 means your audience is seeing it almost 5 times — they're ignoring it now.
> >
> > **Recommendations:**
> > 1. Pause this creative immediately
> > 2. Rotate in 2-3 fresh creatives
> > 3. Consider generating new variants with the [AI Creative Agent](https://github.com/Synter-Media-AI/ai-creative-agent)
>
> **Why CTR drop matters:** When CTR drops, your CPC rises (platforms charge more for less engaging ads). A creative with 2.4% → 1.1% CTR typically costs 2x more per click. Catching this 1 week earlier saves hundreds to thousands.

### 5. Weekly Executive Summary

> **You:** My VP wants a weekly executive summary. Something high-level, not too detailed.
>
> **Agent:** I'll configure a weekly digest designed for executives:
>
> **📈 Weekly Ad Performance — March 17-22, 2026**
>
> **The Big Picture:**
> - Total spend: $8,400 (on budget ✅)
> - Total revenue attributed: $31,920
> - Blended ROAS: 3.8x (up from 3.5x last week ↑)
> - Total conversions: 312 (up 8% ↑)
>
> **Top 3 Wins:**
> 1. 🏆 TikTok ROAS improved 40% after new UGC creative launched
> 2. 📈 Google PMax delivered 22 conversions at $18 CPA (all-time best)
> 3. ✅ Microsoft Ads ROAS hit 5.2x — scaling recommended
>
> **Top 2 Concerns:**
> 1. ⚠️ LinkedIn CPL increasing 3 weeks straight ($68 → $89)
> 2. ⚠️ Meta creative fatigue on 2 of 4 active ads
>
> **Next Week's Action Items:**
> 1. Scale Microsoft Ads budget by 30%
> 2. Refresh Meta creative (2 new variants needed)
> 3. Investigate LinkedIn CPL increase (audience saturation?)
>
> **Delivery:** Every Monday at 8 AM ET to #executive-updates
>
> This gives your VP the 30-second version without drowning in platform-specific details. Want me to customize the format?

---

## Slack Alert Tips

1. **Set up ROAS threshold alerts immediately.** This single alert prevents the most common budget waste — campaigns silently losing money. 1.5x ROAS for warning, 1.0x for automatic pause consideration.
2. **Daily summaries > dashboard checking.** A 30-second Slack summary beats 15 minutes of logging into 4 platforms. Make it a morning ritual.
3. **Alert fatigue is real.** Don't alert on everything. Focus on: ROAS below threshold, budget overspend, creative fatigue, and campaign errors. Ignore normal fluctuations.
4. **Separate channels for different audiences.** #ads-alerts for the media buyer (detailed), #executive-updates for leadership (summary), #creative-alerts for the design team.
5. **Budget pacing alerts save thousands.** A $10,000 monthly budget overspending by 20% costs $2,000 extra. Pacing alerts catch this by day 10, not day 31.
6. **Creative fatigue alerts protect ROAS.** A fatigued creative can double your CPA overnight. Monitor CTR decline and rotate creative before it becomes a problem.
7. **Weekly executive summaries build trust.** VPs love predictable, formatted updates. It shows the marketing team is data-driven and in control.

---

## FAQ

### Is there an MCP for Slack ad alerts?
Yes — this repo. It pre-configures the Synter MCP server for ad performance monitoring and Slack notifications.

### Can AI send me Slack alerts when campaigns underperform?
Yes. Set ROAS thresholds, budget limits, or CTR decline triggers — the agent monitors continuously and alerts your team in Slack.

### Does this connect to all ad platforms?
Yes. Alerts can monitor Google Ads, Meta, LinkedIn, Microsoft, TikTok, Reddit, X, Amazon, and more — all in one Slack channel.

### Can I customize the alert format?
Yes. Choose which metrics to include, which thresholds to trigger on, who to mention, and which Slack channel to post to.

### Does this replace Slack's native Google Ads integration?
It's significantly more powerful. Slack's native integrations are basic notifications. This provides cross-platform comparison, AI-powered anomaly detection, and actionable recommendations.

---

## Related Repos

- [cross-platform-ads-agent](https://github.com/Synter-Media-AI/cross-platform-ads-agent) — The data source for cross-platform reports
- [google-ads-agent](https://github.com/Synter-Media-AI/google-ads-agent) — Google Ads management
- [meta-ads-agent](https://github.com/Synter-Media-AI/meta-ads-agent) — Meta Ads management
- [conversion-tracking-agent](https://github.com/Synter-Media-AI/conversion-tracking-agent) — Tracking verification
- [ai-creative-agent](https://github.com/Synter-Media-AI/ai-creative-agent) — Generate fresh creative when fatigue detected
- [audience-sync-agent](https://github.com/Synter-Media-AI/audience-sync-agent) — Audience management

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
