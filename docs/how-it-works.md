# How it works

Nearly Bot turns a chat message into a live token on NEAR.

```
You (Telegram or X)  ──►  Nearly Bot  ──►  nearly.trade factory  ──►  token + Rhea pool
                                                                      │
                          board · launches channel · X post  ◄────────┘
```

## 1. Get a wallet

- **Telegram**: send `/start` to [@nearlytradebot](https://t.me/nearlytradebot) and accept the terms. The bot
  creates a NEAR wallet for you. You can create more wallets and switch between them (`/wallets`).
- **X**: post `@nearlytradesbot wallet`. The bot replies with your wallet address. Each X account has one wallet.

Fund the wallet with NEAR, or bridge BTC, ETH, SOL, USDC and more into it (see [bridge.md](bridge.md)).
A launch needs about **0.3 NEAR** (storage, fee and gas), plus any first buy.

## 2. Launch

- **Telegram**: `/launch`, then five steps: name, ticker, logo (send a photo), description, first buy. The
  review screen shows the exact cost and lets you set a pair, a trading tax and links. Tap **Launch**.
- **X**: post `@nearlytradesbot launch <name> $<TICKER>`, optionally with a photo and options. See
  [launch-on-x.md](launch-on-x.md).

Nearly Bot checks everything against the factory's rules first. If something's off, it tells you what to fix
and nothing is sent.

## 3. What the launch does on chain

One transaction from your bot wallet calls `launch` on `nearlytrade.near`, the nearly.trade factory, which:

1. creates the token account `<ticker>.nearlytrade.near` (a number is added if the ticker is taken),
2. mints the fixed **1,000,000,000** supply (18 decimals),
3. opens a **Rhea DCL pool** (1% fee tier) holding the whole supply, and
4. makes your optional **first buy**, capped at 4% of supply.

After the launch succeeds, a second transfer pays the Nearly Bot fee. A failed launch isn't charged.

## 4. After launch

- The token appears on the [board](https://nearlybot.com) right away.
- Once its pool is live it's posted in the [launches channel](https://t.me/nearlybotlaunches). Launches made on
  X are also announced by [@nearlytradesbot](https://x.com/nearlytradesbot).
- Anyone can trade it immediately: in the bot, or on the website's **Swap** page with their own wallet.
- As the creator you earn **0.64% of every trade**, paid out automatically about hourly.

## The website

[nearlybot.com](https://nearlybot.com) doesn't launch tokens. It's for:

- **Swap**: buy and sell Nearly Bot tokens with NEAR, from any NEAR wallet (Meteor, HOT, MyNearWallet,
  Ledger, MetaMask and more).
- **Bridge**: move about 200 assets across 30+ chains into and out of NEAR.
- **Board, launches and stats**: every Nearly Bot launch.
- **Connect X**: use your X bot wallet on the website (swap, bridge) or export its private key.
