---
title: YAM Uniswap Farming
description: provide liquidity, stake, get YAMs
published: true
date: 2020-08-29T02:27:52.528Z
tags: 
editor: markdown
---

> The [YAMv1 → YAMv2 migration](/migration) is now over
{.is-info}

# Stake Uniswap LP Shares

Users can provide YAM-yCRV liquidity on Uniswap, then deposit those LP shares into the :rainbow:`Eternal Lands` stakedrop contract to farm even more YAMs.

> Providing YAM liquidity on Uniswap is unsafe! [Remove your funds from Uniswap!][uniswap-warning]
{.is-warning}

LPs for Uniswap pool [0x2c7a51a357d5739c5c74bf3c96816849d2c9f726][etherscan-unipool] are eligible for this stakedrop.  See [markets](/trade) to learn more about this Uniswap pool.

Manage your :rainbow:`Eternal Lands` deposit:
- https://yam.finance/farms (official site)
- https://yieldfarming.info/yam/ycrv/ (independent 3rd party site)
- directly on Etherscan [0xaddbcd6a68bfeb6e312e82b30ce1eb4a54497f4c][etherscan-unipoolstaking]

> Staking from Etherscan requires first setting an allowance from the staked token to the corresponding stake pool
{.is-info}


# Uniswap Stakedrop Rewards

Two-thirds of the YAM supply [will be distributed via this stakedrop](https://medium.com/@yamfinance/yam-finance-d0ad577250c7).  This is equivalent to 3,000,000 of the 5,000,000 "OG YAMs" (that is, YAM that has not been impacted by [rebasing](/rebase)).  In the first week, 1/3rd of the YAM supply will be distributed in this way; the stakedrop continues forever, but each qeek the reward will decrease by an additional 50%.


# How Positive Rebases Impact LPs

Negative `rebase` occurs when the YAM price, according to the Uniswap TWAP oracle for the YAM:yCRV pool, is below $1.  Positive `rebase` occurs when the YAM price, according to the Uniswap TWAP oracle for the YAM:yCRV pool, is above $1.  Read the [rebase](/rebase) article for more context on rebasing.

A negative `rebase` has no impact on Uniswap LPs.

On positive rebases, the [YAM Reserve contract][etherscan-reserve] is supposed to receive 10% of the YAMs that are created by the rebase.  These are funds that YAM tokenholders have to fund governance proposals.

The YAM Reserve doesn't keep the YAMs though, it immediately sells them for yCRV (~$1 USD stablecoin) using the Uniswap YAM:yCRV pool.  If this YAM selling would drop the YAM price in Uniswap by more than 10%, then it only sells enough YAMs to drop the price by 10% and it holds onto the remaining YAMs for future `rebase` cycles.

Unfortunately, the [YAM rebase code was incorrect](/govern#saveyam-vote-delegation); instead of issuing 10% of new YAMs into the YAM Reserve, the YAM Reserve receives a **huge** number of YAMs.  It then uses these huge number of YAMs to buy enough yCRV from the Uniswap pool to drop the YAM price by 10%.  The purchased yCRV is then deposited into the YAM Reserve, which is unfortunately inaccessible due to the rebase bug.

Regardless of how large the positive `rebase` is, a positive rebase will **always** result in the YAM Reserve selling enough YAMs into Uniswap to drop the YAM price there by 10%.




[uniswap-warning]: https://medium.com/@yamfinance/how-to-exit-the-eternal-lands-pool-and-withdraw-your-yam-823d57c95f3a
[etherscan-unipoolstaking]: https://etherscan.io/address/0xaddbcd6a68bfeb6e312e82b30ce1eb4a54497f4c#writeContract
[etherscan-unipool]: https://etherscan.io/address/0x2c7a51a357d5739c5c74bf3c96816849d2c9f726
[etherscan-reserve]: https://etherscan.io/address/0xc53195bbad57105cc9a4df752121afd9c15fbd8f
