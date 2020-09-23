---
title: Yam Treasury
description: on the community treasury 
published: true
date: 2020-09-23T16:21:25.457Z
tags: 
editor: markdown
dateCreated: 2020-09-23T16:21:25.457Z
---

# What is the Treasury?

The treasury is key design element of YAM. The treasury is controlled by YAM holders and funds from it can be applied however YAM Token Holders decide. 

Some examples for YAM Treasury use-cases include investing in yield bearing assets, developing protocols that can enrichen the YAM Ecosystem, deploying liquidity into pools for incentivized farming, and disbursements to YAM Token Holders. 

# How Are Funds Raised for the Treasury?

On every positive rebase, the treasury mints 10% of the rebase amount and sells YAM to the YAM/yUSD Uniswap pool. 

The purchased yUSD is deposited into the YAM treasury, governed by tokenholders. 

For example: 

1. If Current Price is $10 and Target Price is $1, the deviation from the peg is  (10 - 1) / 1 = 9.
2. If the current supply is 5,000,000, then the change in supply will be 5,000,000 * (9/10) = 4,500,000
3. 10% * 4,500,000 would be used to purchase yUSD to send to the treasury, while the other 4,050,000 is distributed to all tokenholders.

There is currently a 10% max slippage amount when the YAM Treasury sells into in the YAM/yUSD pool. When the Treasury allocation exceeds this amount, extra Treasury Funds will be deposited in YAM currency instead. 

# Why Does the Treasury use yUSD?

The treasury uses yUSD (yyCRV) as it’s reserve asset because it is a stable asset with high yield. Using a stable asset (as opposed to ETH for example) allows the treasury to both maintain its value over time as well as grow consistently through high yield. 

# Gitcoin Deposits

YAM Governance has decided to redirect 1% of all inflows to the Treasury  to the Gitcoin Grants Wallet, in order to support public goods in the Ethereum ecosystem. Every funding from the YAM treasury that goes to the Gitcoin Grants wallet will be 100% used for public goods funding for the Ethereum ecosystem. 

# YAM Treasury Deposits 

| Epoch | Date Time    | Treasury Deposit (yUSD) | Treasury Deposit (YAM) | Gitcoin Deposit (yUSD) |  Rebase TX               |
|-------|------------------------------|----------------------|---------------|--------|--------------------------|
| 0     | Sep-18-2020 08:00:00 PM +UTC | ----   | ----     | ----   | ----     

