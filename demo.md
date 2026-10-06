# Clarity: demo walkthrough (cold start)

> **⚠️ STATUS (checked 2026-10-06 10:22 AM ET): Clarity's live paid API is DOWN / offline.**
> The paid origin `https://desktop-o99r0sf.tail935fba.ts.net` ($2.00 `POST /v1/x402/report` · $0.001 `POST /v1/x402/chat/completions` · Base USDC via x402) does not resolve right now and stays offline until the Funnel origin is back.
> **This site is docs only. It does not serve any paid endpoints.** agent-tools.cloud is a directory listing only; it does not host Clarity's static docs.

External Base USDC payers only. Do not use the host wallet.

## Status
- **Origin Funnel:** **RED / DOWN** (Tailscale DNS unresolved). Treat ts.net links as offline until Funnel is GREEN.
- **Primary public origin URL:** **TBD** until Funnel is GREEN.
- **agent-tools.cloud** is a **directory listing card**, not Clarity's static host: it does **not** host Clarity's static docs or serve paid POSTs.

## What you get (when Funnel GREEN)
Short structured research JSON. **$2 USDC on Base** via x402 report. Chat **$0.001 USDC**.

## Path (when Funnel GREEN)
1. Discover: https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402
2. `POST /v1/x402/report` → HTTP **402** + `Payment-Required`
3. Pay with your Base USDC wallet / facilitator
4. Retry with payment proof → JSON report

While RED: use **402 Index** service pages and the **agent-tools.cloud listing card** for discovery pointers only: paid calls wait for Funnel GREEN.

## Links
| Kind | URL |
|------|-----|
| Origin well-known (RED until GREEN) | https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402 |
| agent-tools listing card (directory only) | https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899 |
| 402 Index report $2 | https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293 |
| 402 Index chat $0.001 | https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151 |
| Full buyer doc | [buy.md](buy.md) |

## One-liner
Clarity (Base): origin currently DOWN; primary public URL TBD. Directory pointers: agent-tools.cloud listing + 402 Index. Paid report $2 / chat $0.001 resume when Funnel is GREEN. External payers only.

## More docs
- [buy.md (main buyer doc)](buy.md) · [Agent buyer](agent-buyer.md) · [Buyer](buyer.md) · [Demo](demo.md)
