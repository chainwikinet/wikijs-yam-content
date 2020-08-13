---
title: YAM Rebasing
description: 1 YAM = $1 ???
published: true
date: 2020-08-13T21:26:51.831Z
tags: 
editor: markdown
---

# Supply Scaling Factor

Many values in the YAM Protocol (under the hood) are denominated in "OG (uninflated) YAM supply" (OG Supply), which is 5,000,000 YAMs that were originally planned for stakedropping.

A variable called `yamsScalingFactor` in the YAM contract sets the value by which OG Supply is multiplied to get the YAM balance value that you see in wallets and UIs.  In the contract, this variable is scaled by x 10**-18:

https://etherscan.io/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16#readContract

# Scaling Factor History

| Epoch | datetime                     | Scaling Factor       | Rebase TX                |
|-------|------------------------------|----------------------|--------------------------|
| 1     | Aug-12-2020 08:00:08 PM +UTC | 9307350094489455602  | [0x7b9017ec...][rebase1] |
| 2     | Aug-13-2020 08:00:18 AM +UTC | 18780439270761214101 | [0x32735e9e...][rebase2] |
| 3     | Aug-13-2020 08:00:24 PM +UTC | 17889705531675302598 | [0x527b8a97...][rebase3] |
| 4     | Aug-14-2020 08:00:00 AM +UTC | ...                  | [...][rebase4] |
| 5     | Aug-14-2020 08:00:00 PM +UTC | ...                  | [...][rebase5] |
| 6     | Aug-15-2020 08:00:00 AM +UTC | ...                  | [...][rebase6] |
| 7     | Aug-15-2020 08:00:00 PM +UTC | ...                  | [...][rebase7] |
| 8     | Aug-16-2020 08:00:00 AM +UTC | ...                  | [...][rebase8] |

[rebase1]: https://etherscan.io/tx/0x7b9017ec92b0200455e5269380195fbecfbf91c8acda30985cc1dc413d215076
[rebase2]: https://etherscan.io/tx/0x32735e9e9aac51739b5725a225be6c7a3851f422be986d0f4f4bc0ec475ee286
[rebase3]: https://etherscan.io/tx/0x527b8a970a53bd46d99d758aa16ff9c2218513b46647a7cfbff72f8a22f8aedc
[rebase4]: #
[rebase5]: #
[rebase6]: #
[rebase7]: #
[rebase8]: #
