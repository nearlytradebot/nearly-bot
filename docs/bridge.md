# Bridge

Nearly Bot bridges about 200 assets across 30+ chains (BTC, ETH, SOL, USDC, USDT and more) into and out of
NEAR through [NEAR Intents](https://near-intents.org) (1Click).

## How a bridge works

1. You get a one-time **deposit address** for this bridge only.
2. You send the asset there, from any wallet or exchange.
3. Solvers deliver it to the recipient, usually within minutes. Bitcoin waits for confirmations.
4. If it can't be completed before the deadline, your deposit is **refunded** to your refund address.

Some chains also need a **memo** with the deposit. It's shown next to the address; deposits without it can't be
matched.

## Where

| Where | Into NEAR | Out of NEAR |
| --- | --- | --- |
| Website, Bridge page | Get a deposit address and QR code; send from anything. Receive NEAR, USDC or USDT on NEAR | Connect a NEAR wallet, review the quote, sign one transaction |
| Telegram | `/bridge` → pick a route, or one line: `/bridge 0.01 BTC refund <your BTC address>` | `/bridge out 5 NEAR to USDC on base 0x…` (asks you to confirm) |
| X | `@nearlytradesbot bridge 0.01 BTC refund <address>` | `@nearlytradesbot bridge out 5 NEAR to USDC on base 0x…` (sends right away) |

In the bots, bridged NEAR lands in your bot wallet, and the bot messages you (or replies on X) when it arrives.

One-line syntax, used by both bots:

```
bridge [in] <amount> <ASSET> [on <chain>] [refund] <address>
bridge out <amount|max> [NEAR] to <ASSET> [on <chain>] <address>
```

Add `on <chain>` for assets that exist on several chains, for example `50 USDC on base`.

## Fees

Every quote already includes bridge and solver costs and the **0.5%** Nearly Bot bridge fee. What you see is
what you get, within the quoted slippage (1%).
