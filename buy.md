# Clarity: for external x402 payers

> **✅ STATUS (checked 2026-10-13 ~10:50 AM ET): Clarity's paid API is LIVE** at [https://desktop-o99r0sf.tail935fba.ts.net](https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402): $2.00 `POST /v1/x402/report` · $0.001 `POST /v1/x402/chat/completions` · Base USDC via x402, external payers only.
> Uptime depends on Lauren's desktop being online, so the origin can go offline without notice.
> **This site is docs only. It does not serve any paid endpoints.** agent-tools.cloud is a directory listing only; it does not host Clarity's static docs.

Bring your own Base USDC. Do not use the host wallet.

## Status
- **Origin (Tailscale Funnel):** **LIVE** as of 2026-10-13 ~10:50 AM ET: `/health`, `/.well-known/x402`, `/static/buy.md` return 200; unpaid POST returns 402. Depends on Lauren's desktop being online.
- **Primary public origin URL:** https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402
- **Directory / index cards** (always up). These are **not** Clarity's static host and do **not** serve paid calls:
  - agent-tools.cloud listing card: https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899
  - 402 Index report: https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293
  - 402 Index chat: https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151

## One-liner
Clarity (Base mainnet x402): paid API live at https://desktop-o99r0sf.tail935fba.ts.net (`POST /v1/x402/report` $2 · `POST /v1/x402/chat/completions` $0.001). Directory cards: agent-tools.cloud + 402 Index. Uptime depends on Lauren's desktop. External Base USDC payers only.

## Paid products
| Product | Price | Method | Path |
|---------|-------|--------|------|
| Research report | $2.00 USDC | POST | `/v1/x402/report` |
| Chat completions | $0.001 USDC | POST | `/v1/x402/chat/completions` |

## Discovery
| Kind | URL | Status |
|------|-----|--------|
| Funnel well-known | https://desktop-o99r0sf.tail935fba.ts.net/.well-known/x402 | **LIVE** (desktop-dependent) |
| agent-tools.cloud | https://agent-tools.cloud/services/desktop-o99r0sf-tail935fba-ts-net-sub899 | Directory listing card only |
| 402 Index report | https://402index.io/service/064c4c86-74e3-4a3e-8814-c76f403da293 | Index page |
| 402 Index chat | https://402index.io/service/03ccd3cc-fda5-414f-a88f-95c39c61e151 | Index page |

## Smoke test
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
