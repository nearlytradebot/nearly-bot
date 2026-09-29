# Launching from X

One post to [@nearlytradesbot](https://x.com/nearlytradesbot) launches a real nearly.trade token.

## 1. Get your wallet

Post:

```
@nearlytradesbot wallet
```

The bot replies with your wallet address. Send it about **0.3 NEAR** (plus any first buy). Each X account has
exactly one wallet.

## 2. Post the launch

Name first, then `$TICKER`, then any options in any order. Attach a photo to use it as the logo.

```
@nearlytradesbot launch Moon Cat $MCAT
```

| Add | Write | Rule |
| --- | --- | --- |
| Logo | attach a photo | Stored on chain as the token logo |
| Description | `desc "Your text"` | Up to 500 characters, in quotes |
| Website | `site https://…` | Any https:// link |
| X link | `x https://x.com/…` | Defaults to your X profile |
| Telegram | `tg https://t.me/…` | Your community link |
| First buy | `first buy 2` | NEAR bought at launch; NEAR pair only; up to 4% of supply |
| Pair | `pair usdc`, `pair tsla` | NEAR (default), NEARLY, ZEC, RHEA, KAT, USDC, USDT, BTC, ETH, GOLD, SILVER, HOOD, or a tokenized stock: NVDA, TSLA, AAPL, SPY, MSFT, META, GOOGL, AMZN, QQQ, CRCL, MRVL, AGG, IAU, TIP, TLT, INTC, SGOV |
| Tax | `tax 2/2` | Buy / sell tax, 0–4% each, all to you |
| Tax split | `tax 2/2 split 50/25/25` | Creator / burn / holders, must total 100 |

Full example:

```
@nearlytradesbot launch Moon Cat $MCAT desc "The cat that went to the moon" site https://mooncat.xyz first buy 1 tax 2/2 split 50/50/0
```

## 3. Get the reply

Within a couple of minutes the bot replies with your token page and announces the launch on X. It's also
posted in the [launches channel](https://t.me/nearlybotlaunches) and listed on the
[board](https://nearlybot.pages.dev).

## Notes

- Keep the post under 280 characters.
- Tax can't be changed after launch.
- If an option breaks a rule, the bot replies with what to fix. Nothing is sent or charged.

## More from X

| Post | What it does |
| --- | --- |
| `@nearlytradesbot wallet` | Your wallet address and balance |
| `@nearlytradesbot name alice` | Claim `alice.nearlytradebot.near` (0.02 NEAR) |
| `@nearlytradesbot bridge 0.01 BTC refund <your BTC address>` | Bridge BTC into your wallet as NEAR |
| `@nearlytradesbot bridge out 5 NEAR to USDC on base 0x…` | Send NEAR out as USDC on Base |
| `@nearlytradesbot help` | The command list |

On the website, **Portfolio → Connect X** shows your X wallet's address and balance (view only).
