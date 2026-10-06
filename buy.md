# Clarity: for external x402 payers

> **⚠️ STATUS (checked 2026-10-06 10:22 AM ET): Clarity's live paid API is DOWN / offline.**
> The paid origin `https://desktop-o99r0sf.tail935fba.ts.net` ($2.00 `POST /v1/x402/report` · $0.001 `POST /v1/x402/chat/completions` · Base USDC via x402) does not resolve right now and stays offline until the Funnel origin is back.
> **This site is docs only. It does not serve any paid endpoints.** agent-tools.cloud is a directory listing only; it does not host Clarity's static docs.

Bring your own Base USDC. Do not use the host wallet.

## Status
- **Origin Funnel (Tailscale):** **RED / DOWN**. `desktop-o99r0sf.tail935fba.ts.net` does not resolve. Treat ts.net links as offline until Funnel is **GREEN**.
- **Primary public origin URL:** **TBD** until the Funnel origin recovers (then: `https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402`).
- **What stays usable while RED:** directory / index cards. These are **not** Clarity's static host and do **not** serve paid calls:
  - agent-tools.cloud listing card: https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899
  - 402 Index report: https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293
  - 402 Index chat: https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151

## One-liner
Clarity (Base mainnet x402): origin currently **DOWN**. Directory cards: agent-tools.cloud + 402 Index. Paid paths (`POST /v1/x402/report` $2 · `POST /v1/x402/chat/completions` $0.001) resume when the origin is back. External Base USDC payers only.

## Paid products (Funnel origin: offline until GREEN)
| Product | Price | Method | Path |
|---------|-------|--------|------|
| Research report | $2.00 USDC | POST | `/v1/x402/report` |
| Chat completions | $0.001 USDC | POST | `/v1/x402/chat/completions` |

## Discovery
| Kind | URL | Status |
|------|-----|--------|
| Funnel well-known | https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402 | **RED / offline** |
| agent-tools.cloud | https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899 | Directory listing card only |
| 402 Index report | https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293 | Index page |
| 402 Index chat | https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151 | Index page |

## Smoke test (only once the origin is back)
```bash
curl -sS -i https://desktop-o99r0sf.tail935fba.ts.net/v1/x402/report \
  -H 'Content-Type: application/json' \
  -d '{"topic":"x402 agent commerce on Base","max_words":400}'
```
Expected: HTTP **402** with a `Payment-Required` header, then retry with payment proof.

## Where it is listed (directories, not the origin)
- **agent-tools.cloud**: listing card (does not host Clarity static docs): https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899
- **402 Index**: report + chat service pages above
- **x402-list**: slug `clarity`, https://x402-list.com
- **TechTools.cz #1104**: https://techtools.cz/tools/launchpad/?tool=1104
- **CurlShip**: https://curlship.com/l/3737
- **AI Product Index**: https://index.percall.dev/l/clarity-x402-base.html

## More docs
- [Agent buyer walkthrough](agent-buyer.md)
- [Buyer walkthrough](buyer.md)
- [Demo walkthrough](demo.md)
