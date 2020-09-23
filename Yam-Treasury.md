---
title: Yam Treasury
description: on the community treasury 
published: true
date: 2020-09-23T16:42:26.051Z
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

# YAM Treasury Inflow 

YAM Treasury inflow only happen during positive rebases. Here's a list of inflow so far!

| Epoch | Date Time    | Treasury Inflow (yUSD) | Treasury Inflow (YAM) | Gitcoin Inflow (yUSD) |  Rebase TX               |
|-------|------------------------------|----------------------|---------------|--------|--------------------------|
| 1     | Sep-21-2020 08:00:08 PM +UTC | 496,734  | 214,321     | 4,967   | [0x9dac453a...][rebase_1] |    
| 2     | Sep-22-2020 08:01:20 AM +UTC | 191,258  | 204,284     | 1,912   | [0x9dac453a...][rebase_2] |    
| 3     | Sep-22-2020 08:00:31 PM +UTC | 189,155  | 76,671     | 1,891   | [0x9dac453a...][rebase_3] |  

[rebase_1]: https://etherscan.io/tx/0x9dac453a1f26125525ca048f96c472e2883252de974ec382d76086f19eba25a9
[rebase_2]: 
https://etherscan.io/tx/0x1ea2025fb21ad277983b745d747345a2cc7e85aab55a45745985f90b926d5b93
[rebase_3]: 
https://etherscan.io/tx/0x3c0995865aaa965713dba860e569c2af0b2b72a130f5c667100500e01d72714a

