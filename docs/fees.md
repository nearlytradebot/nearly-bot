# Fees

| What | Amount | Goes to |
| --- | --- | --- |
| Launch fee | **0.05 NEAR** per launch | Nearly Bot. On Telegram bot launches by someone you invited, **0.01 NEAR** of it goes to you ([referrals.md](referrals.md)) |
| Launch storage | About **0.16 NEAR** (up to about 0.37 NEAR with a full 16 KB logo and a tax) | NEAR storage for the token and its pool |
| First buy | Optional, your choice (up to 4% of supply) | You buy your own token as the pool opens |
| Custom wallet name | **0.02 NEAR**, once | Nearly Bot |
| Swap (buy or sell) | **0.5%** of the NEAR side of each trade, on the website and in the Telegram bot | Nearly Bot |
| Bridge | **0.5%** of each bridge, included in the quote | Nearly Bot |
| Bridge network costs | Included in each quote | NEAR Intents solvers |
| Trading | The pool's **1%** fee on each trade | **0.64% to the token's creator**; the rest to nearly.trade and Rhea |
| Token tax | Optional, 0–4% per side, set at launch | Creator, burn and/or holders |
| Gas | Usually well under 0.01 NEAR | NEAR validators |

## How the launch fee is paid

The fee is a separate transfer made **after** the launch succeeds, so a failed launch costs nothing. The bot
shows the exact total (storage, fee and any first buy) before you confirm.

## How the swap fee is paid

On a **buy**, 0.5% of the NEAR you spend goes to Nearly Bot and the rest is swapped. On a **sell**, 0.5% of the
NEAR you receive goes to Nearly Bot. The website shows the fee before you sign; in the Telegram bot it's taken
only after the swap goes through, so a refunded swap pays nothing.

## Where Nearly Bot's fees go

All fees Nearly Bot collects (launch, custom name, swap and bridge fees, after referral rewards) are used for
**buybacks, burns and platform development**.

Fees are paid to [`nearlytradebot.near`](https://nearblocks.io/address/nearlytradebot.near), so every payment
is public on NearBlocks.
