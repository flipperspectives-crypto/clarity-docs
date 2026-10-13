# Clarity: buyer walkthrough (cold start)

> **✅ STATUS (checked 2026-10-13 ~10:50 AM ET): Clarity's paid API is LIVE** at [https://desktop-o99r0sf.tail935fba.ts.net](https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402): $2.00 `POST /v1/x402/report` · $0.001 `POST /v1/x402/chat/completions` · Base USDC via x402, external payers only.
> Uptime depends on Lauren's desktop being online, so the origin can go offline without notice.
> **This site is docs only. It does not serve any paid endpoints.** agent-tools.cloud is a directory listing only; it does not host Clarity's static docs.

External Base USDC payers only. Do not use the host wallet.

## Status
- **Origin (Tailscale Funnel):** **LIVE** as of 2026-10-13 ~10:50 AM ET. Depends on Lauren's desktop being online, so it can go offline.
- **Primary public origin URL:** https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402
- **agent-tools.cloud** is a **directory listing card**, not Clarity's static host: it does **not** host Clarity's static docs or serve paid POSTs.

## What you get
Short structured research JSON. **$2 USDC on Base** via x402 report. Chat **$0.001 USDC**.

## Path
1. Discover: https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402
2. `POST /v1/x402/report` → HTTP **402** + `Payment-Required`
3. Pay with your Base USDC wallet / facilitator
4. Retry with payment proof → JSON report

Discovery pointers also on **402 Index** service pages and the **agent-tools.cloud listing card** (directory only; paid calls go to the origin).

## Links
| Kind | URL |
|------|-----|
| Origin well-known (live, desktop-dependent) | https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402 |
| agent-tools listing card (directory only) | https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899 |
| 402 Index report $2 | https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293 |
| 402 Index chat $0.001 | https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151 |
| Full buyer doc | [buy.md](buy.md) |

## One-liner
Clarity (Base): paid API live at https://desktop-o99r0sf.tail935fba.ts.net (report $2 / chat $0.001). Directory pointers: agent-tools.cloud listing + 402 Index. Uptime depends on Lauren's desktop. External payers only.

## More docs
- [buy.md (main buyer doc)](buy.md) · [Agent buyer](agent-buyer.md) · [Buyer](buyer.md) · [Demo](demo.md)
