---
title: YAM Total Supply
description: how many YAMs are there
published: true
date: 2020-08-16T22:09:16.263Z
tags: 
editor: markdown
---

# How Many YAMs are there?

This has a simple answer and a more complicated answer.

The simple answer is that there are 5,000,000 YAMs... before considering rebasing.

OG YAM distribution plan (described in https://medium.com/@yamfinance/yam-finance-d0ad577250c7):

```
5,000,000 max supply
====================
2,000,000 distributed in week1 via stakedrops (deposit regular tokens, get YAMs)
3,000,000 distributed via Uniswap LP stakedrop
----------------------------------------------
1,500,000 distributed in week1 via Uniswap LP stakedrop
  750,000 distributed in week2 via Uniswap LP stakedrop
  375,000 distributed in week3 via Uniswap LP stakedrop
  187,500 distributed in week4 via Uniswap LP stakedrop
   93,750 distributed in week5 via Uniswap LP stakedrop
   46,875 distributed in week6 via Uniswap LP stakedrop
   ...... continues forever, halving each week
```

# How many YAMs are there right this second?

As of right now (2020-08-16 22:00 GMT):
- total supply is approximately 73,400,000 YAMS
- approximately 51,500,000 YAMs have been distributed



# How to convert from YAM balance to OG YAMs?

Everything in OG YAM terms stays the same regardless of rebases, but everything in current YAM balance will keep changing as rebases occur.

This thread provides an overview of how to calculate supply using the various values you can get from the YAM token contract https://twitter.com/bcmakes/status/1295066620318998533

To transform OG YAM balance into current YAM balances, get `yamsScalingFactor` and `base` from https://etherscan.io/address/0x0e2298e3b3390e3b945a5456fbf59ecc3f55da16#readContract

Multiply OG YAM balance by `yamsScalingFactor` and then divide by `base`.