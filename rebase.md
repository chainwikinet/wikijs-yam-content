---
title: YAM Rebasing
description: 1 YAM = $1 ???
published: true
date: 2020-08-14T01:02:54.441Z
tags: 
editor: markdown
---

# What Is Rebasing?

YAM changes the balance of everyone's wallets to try to reach a price of $1.  This process is called "rebasing" and is similar to the mechanism used by [Ampleforth](https://www.ampleforth.org/).  YAM rebases—and your wallet balance of YAMs may change—every 12 hours.

Rebasing works like this:

1. if YAM is selling for more than $1, increase the number of YAMs to make YAM more common.  The balance of YAMs in all wallets and contracts will increase.

2. if YAM is selling for less than $1, decrease the number of YAMs to make YAM more rare.  The balance of YAMs in all wallets and contracts will decrease.

3. if YAM is selling for approximately $1, keep the YAM balances the same.

# Supply Scaling Factor

The balance of YAMs in wallets and contracts is adjusted in the rebasing process by changing a variable called `yamScalingFactor` in the YAM contract.

`yamScalingFactor` is the value by which "OG YAM supply" (5,000,000 YAM originally planned for stakedropping) is multiplied in order to get the YAM balance value that you see in wallets, contracts, and other UIs.  

In the contract, this `yamScalingFactor` variable is scaled by x 10**-18: https://etherscan.io/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16#readContract

In YAM governance, values such as `votes` are denominated in OG Supply instead of in wallet balance.

# Scaling Factor History

| Epoch | datetime                     | Scaling Factor       | Effect On Balances | Rebase TX                |
|-------|------------------------------|----------------------|--------------------|--------------------------|
| 1     | Aug-12-2020 08:00:08 PM +UTC | 9307350094489455602  | increase ~9.3x     | [0x7b9017ec...][rebase1] |
| 2     | Aug-13-2020 08:00:18 AM +UTC | 18780439270761214101 | increase ~2.0x     | [0x32735e9e...][rebase2] |
| 3     | Aug-13-2020 08:00:24 PM +UTC | 17889705531675302598 | decrease ~5%       | [0x527b8a97...][rebase3] |
| 4     | Aug-14-2020 08:00:00 AM +UTC | ...                  | ...                | [...][rebase4]           |
| 5     | Aug-14-2020 08:00:00 PM +UTC | ...                  | ...                | [...][rebase5]           |
| 6     | Aug-15-2020 08:00:00 AM +UTC | ...                  | ...                | [...][rebase6]           |
| 7     | Aug-15-2020 08:00:00 PM +UTC | ...                  | ...                | [...][rebase7]           |
| 8     | Aug-16-2020 08:00:00 AM +UTC | ...                  | ...                | [...][rebase8]           |

[rebase1]: https://etherscan.io/tx/0x7b9017ec92b0200455e5269380195fbecfbf91c8acda30985cc1dc413d215076
[rebase2]: https://etherscan.io/tx/0x32735e9e9aac51739b5725a225be6c7a3851f422be986d0f4f4bc0ec475ee286
[rebase3]: https://etherscan.io/tx/0x527b8a970a53bd46d99d758aa16ff9c2218513b46647a7cfbff72f8a22f8aedc
[rebase4]: #
[rebase5]: #
[rebase6]: #
[rebase7]: #
[rebase8]: #
