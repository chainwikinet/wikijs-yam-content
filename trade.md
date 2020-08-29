---
title: YAM Markets
description: trade YAMs
published: true
date: 2020-08-29T02:27:41.319Z
tags: 
editor: markdown
---

# YAMv2

This is the YAMv2 token: https://etherscan.io/token/0xaba8cac6866b83ae4eec97dd07ed254282f6ad8a

> verify the token address in multiple places — don't get tricked by fake YAMs!
{.is-warning}

Trade for YAMv2 on Uniswap: https://app.uniswap.org/#/swap?outputCurrency=0xaba8cac6866b83ae4eec97dd07ed254282f6ad8a

YAMv2 market dashboards:
- https://www.coingecko.com/en/coins/yam-v2
- https://coinmarketcap.com/currencies/yam-v2
- https://uniswap.info/token/0xaba8cac6866b83ae4eec97dd07ed254282f6ad8a


# YAMv1

> YAMv1 can still be bought and sold, but migration from YAMv1 to YAMv2 has closed and YAMv1 can no longer be converted to YAMv2. YAMv1 information is preserved below for informational purposes.
{.is-info}

## YAMv1 Token

This is the YAMv1 token: https://etherscan.io/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16

The YAMv1 token is an upgradeable proxy token, which is a permanent address that can be adjusted to point at a new implementation address that encodes new token logic.  The current YAM token implementation contract is stored in a variable called `implementation` in the YAM proxy contract.

The current YAMv1 token implementation contract: https://etherscan.io/address/0xa923af6d05993495257a872ec69dbbf01501eb0e

## YAMv1 Uniswap

Trade for YAMv2 on Uniswap: https://app.uniswap.org/#/swap?outputCurrency=0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16

YAMv1 market dashboards:
- https://www.coingecko.com/en/coins/yam
- https://coinmarketcap.com/currencies/yam
- YAMv1 on Uniswap: https://uniswap.info/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16
- "official" YAMv1:yCRV pool: https://uniswap.info/pair/0x2c7a51a357d5739c5c74bf3c96816849d2c9f726


## YAMv1 Uniswap LP Warnings

> Providing liquidity on Uniswap is for advanced users. You may lose funds! Understand the risks before attempting!
{.is-warning}

There were concerns that a problem in the [YAMv1 rebasing contract](/rebase) could cause issues for liquidity providers (LPs) in the YAM:yCRV Uniswap pool (YAM-yDAI+yUSDC+yUSDT+yTUSD Pair) if YAMv1 underwent a positive rebase.  These concerns are no longer valid because positive rebasing is now broken.

Some pools were not recognized by the [YAMv1 rebaser contract](/rebase), and therefore LPs providing liquidity in these pools were NOT guaranteed to receive their share of positive rebases.  This includes the [YAMv1-ETH pool](https://uniswap.info/pair/0xc358001a71b3160b4b243d6e8c6f52579f82215e).  However, positive rebasing is now broken and this is no longer a concern.







[uniswap-warning]: https://medium.com/@yamfinance/how-to-exit-the-eternal-lands-pool-and-withdraw-your-yam-823d57c95f3a