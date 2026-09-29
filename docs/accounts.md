# On-chain accounts

All on NEAR mainnet.

| Role | Account |
| --- | --- |
| Launch factory (nearly.trade) | [`nearlytrade.near`](https://nearblocks.io/address/nearlytrade.near) |
| Pools (Rhea DCL exchange) | [`dclv2.ref-labs.near`](https://nearblocks.io/address/dclv2.ref-labs.near) |
| Wrapped NEAR | [`wrap.near`](https://nearblocks.io/address/wrap.near) |
| Nearly Bot fees and custom wallet names | [`nearlytradebot.near`](https://nearblocks.io/address/nearlytradebot.near) |
| Tokens | `<ticker>.nearlytrade.near` (NEP-141, 1,000,000,000 supply, 18 decimals) |
| Custom wallet names | `<name>.nearlytradebot.near` |

Nearly Bot deploys no contract of its own. Every token is created by the nearly.trade factory.

## Verify a launch

1. **It's a nearly.trade token.** The token account ends in `.nearlytrade.near`: only the factory can create
   accounts under it.
2. **Read its launch record from the factory**, for example with [NEAR CLI](https://near.cli.rs):

   ```bash
   near contract call-function as-read-only nearlytrade.near get_launch_by_token \
     json-args '{"token":"mcat.nearlytrade.near"}' network-config mainnet now
   ```

   It shows the creator, the total supply, the pool, the first buy and whether the launch is done (`step`).
   For the tax, call `get_tax` with `{"launch_id":"<id>"}` using the `id` from that record.
3. **Check it on [NearBlocks](https://nearblocks.io)**: open the token account to see its supply, holders and
   the launch transaction to `nearlytrade.near`.
4. **Check it's a Nearly Bot launch.** Only launches made through the Telegram bot or X are on the
   [board](https://nearlybot.com); each one links to its token page.
5. **Check the fee.** The Nearly Bot fee for each launch is a plain transfer to `nearlytradebot.near`,
   visible on NearBlocks.
