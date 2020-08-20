---
title: YAMv2 Migration
description: convert YAMv1 → YAMv2
published: true
date: 2020-08-20T00:22:49.258Z
tags: 
editor: markdown
---


> YAMv2 migration is underway!  Migrate your YAM tokens ASAP!
{.is-danger}


# What You Need To Do

> Leave enough time before the deadline to ensure that your migration transactions confirm with plenty of time to spare.  Migrations that confirm after the deadline will fail!
{.is-warning}

You have a three-day (72 hour) window to migrate your YAM tokens to YAMv2.

The clock is already ticking, so do not delay—migrate now.


## 1. Don't get YAM scammed

People may try to trick you out of your YAMs.

Before you take any action, verify that this article is legitimate!

- https://twitter.com/YamFinance/status/1296129003405938693
- https://medium.com/@yamfinance/yam-migration-live-955c63766ab8

## 2. Move YAM into your wallet

Move all YAM tokens into your wallet before you migrate them.

- withdraw from centralized exchanges into a wallet that you control, such as Metamask or Trust.
- "harvest" any YAMs that you farmed at [yam.finance](https://yam.finance/farms).  You don't have to unstake the collateral that you used to farm, but [Wave1 farming is over](/stakedrop) and it is no longer farming additional YAMs.
- harvest and withdraw Uniswap LP shares from the :rainbow:`Eternal Lands` pool.
- remove YAM liquidity from any Uniswap pools, especially the [YAM:yCRV Uniswap pool](https://app.uniswap.org/#/remove/0x0e2298e3b3390e3b945a5456fbf59ecc3f55da16/0xdf5e0e81dff6faf3a7e52ba697820c5e32d806a8).  This pool is still farming new YAMs as part of [Wave2 staking](/stakedrop-uniswap), but all YAMs MUST be harvested and migrated before the deadline.

## 3. Add the new YAMv2 token to your wallet

Because YAMv2 is new, some wallets may not display the YAMv2 token immediately after migration.

To add YAMv2 in Metamask, [follow these instructions to add a custom token](https://metamask.zendesk.com/hc/en-us/articles/360015489031-How-to-View-See-Your-Tokens-in-Metamask) and paste in the YAMv2 token address when requested: `0xaba8cac6866b83ae4eec97dd07ed254282f6ad8a`

Alternatively, after migration, view your Ethereum wallet address on [Etherscan](https://etherscan.io) and look in the token dropdown for YAMv2.


## 4. Migrate on [yam.finance](https://yam.finance)

> Migration requires two transactions.  Perform both transactions to migrate!
{.is-info}

Follow the instructions on [yam.finance](https://yam.finance) to connect your wallet and perform the migration.

In the migration, your YAM will be exchanged for YAMv2.

> [Due to rebasing](/rebase), you will receive 1 YAMv2 for every ~10 YAM that you migrate.
{.is-info}

The first transaction will call `approve` on the YAMv1 token contract, `0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16`.  It allows the migration contract to manage your tokens.

The second transaction will call `migrate` on the migration contract, `0xf1d7c9E4c57a5C1902f4A4aE2630d2Da78Ffb1c1`.  It will exchange your YAM tokens for YAMv2 tokens.

## 5. Listen for official announcements

> A timeline for the migration from YAMv2 to YAMv3 has not been announced.  Don't get YAM scammed!
{.is-warning}

Follow the [official yam.finance social media accounts and Discord chat](/team) for announcements.  Come hang out with us on Discord!  Contribute to this wiki!

Migration from YAMv2 to YAMv3 will probably not have a deadline, so don't believe anyone that tries to trick you into giving up your YAM.








