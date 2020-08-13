---
title: YAM Markets
description: trade YAMs
published: true
date: 2020-08-13T21:19:29.160Z
tags: 
editor: markdown
---

# YAM Token
This is the YAM token: https://etherscan.io/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16

> verify the token address in multiple places — don't get tricked by fake YAMs!
{.is-warning}

The YAM token is an upgradeable proxy token, which is a permanent address that can be adjusted to point at a new implementation address that encodes new token logic.  The current YAM token implementation contract is stored in a variable called `implementation` in the YAM proxy contract.

The current YAM token implementation contract: https://etherscan.io/address/0xa923af6d05993495257a872ec69dbbf01501eb0e

YAM market dashboards:
- https://www.coingecko.com/en/coins/yam
- https://coinmarketcap.com/currencies/yam/

# Uniswap

> Providing YAM liquidity on Uniswap is unsafe! [Remove your funds from Uniswap!][uniswap-warning]
{.is-warning}

YAM is available to trade on Uniswap.

YAM Uniswap pool information: https://uniswap.info/token/0x0e2298e3b3390e3b945a5456fbf59ecc3f55da16

While it is currently safe to **trade** YAM on Uniswap, it is NOT SAFE to **provide liquidity** to YAM Uniswap pools.

Some pools are not recognized by the [YAM rebaser contract](/rebase), and therefore LPs providing liquidity in these pools are NOT guaranteed to receive their share of positive rebases.  This includes the YAM-ETH pool: https://uniswap.info/pair/0xc358001a71b3160b4b243d6e8c6f52579f82215e

Due to a problem with the [YAM rebaser contract](/rebase), providing liquidity to the YAM-yCRV pool (YAM-yDAI+yUSDC+yUSDT+yTUSD Pair) is also **dangerous** and may result in loss of funds due to rebasing!

https://uniswap.info/pair/0x2c7a51a357d5739c5c74bf3c96816849d2c9f726

[uniswap-warning]: https://medium.com/@yamfinance/how-to-exit-the-eternal-lands-pool-and-withdraw-your-yam-823d57c95f3a