# Launching and trading on Telegram

Open [@nearlytradebot](https://t.me/nearlytradebot) and send `/start`. Everything is a panel you tap through.

## Launch

`/launch` walks you through five steps:

| Step | What to send | Rules |
| --- | --- | --- |
| Name | Text | 1–32 characters |
| Ticker | Text | 2–10 letters or digits |
| Logo | A photo (or Skip) | Stored on chain, 16 KB max |
| Description | Text (or Skip) | Up to 500 characters |
| First buy | NEAR amount (or Skip) | Up to 4% of supply (about 42.9 NEAR); NEAR pair only |

The review screen shows the full cost and lets you change:

- **Pair**: NEAR (default), NEARLY, ZEC, RHEA, KAT, USDC, USDT, BTC, ETH, GOLD, SILVER, HOOD, or a tokenized stock: NVDA, TSLA, AAPL, SPY, MSFT, META, GOOGL, AMZN, QQQ, CRCL, MRVL, AGG, IAU, TIP, TLT, INTC, SGOV. Stocks are under **📈 Stocks** in the pair picker.
- **Tax**: 0–4% on buys and sells, split between creator, burn and holders. It can't be changed later.
- **Links**: website, X and Telegram.

Shortcut: `/launch Moon Cat | MCAT` fills in the name and ticker.

## Trade

Paste a token contract (`mcat.nearlytrade.near`) or a ticker (`$MCAT`) to open its panel: price, market cap,
volume, tax, your holdings, quick-buy buttons and sell 25/50/100%.

## Commands

| Command | What it does |
| --- | --- |
| `/start` | Home panel |
| `/launch` | Launch a token |
| `/buy TICKER 5` | Buy with 5 NEAR |
| `/sell TICKER 50%` | Sell half your holding |
| `/positions` | Your holdings, valued in NEAR |
| `/tokens` | Newest Nearly Bot launches |
| `/wallet` | Deposit, withdraw, unwrap wNEAR |
| `/wallets` | Switch between your wallets, or add one |
| `/import` | Add your own wallet by private key or seed phrase |
| `/bridge` | Bridge in or out (see [bridge.md](bridge.md)) |
| `/name alice` | Claim `alice.nearlytradebot.near` (0.02 NEAR) |
| `/invite` | Your invite link and earnings (see [referrals.md](referrals.md)) |
| `/settings` | Slippage (1/2/5/10%) and quick-buy amounts |
| `/cancel` | Stop the current step |
| `/help` | Everything above |

## Several wallets

**Wallet → My wallets** (or `/wallets`) lists your wallets with their balances. Tap one to make it active,
or **New wallet** to add one (up to 10). Launches, trades, bridges and withdrawals always use the active wallet.
`/import` adds a wallet you already own as another wallet; your other wallets stay. Send its private key
(`ed25519:…`) or its 12/24-word seed phrase, and the bot finds the account. If the key controls more than one
account, put the account name first: `name.near ed25519:…`. The bot deletes your message right away.
