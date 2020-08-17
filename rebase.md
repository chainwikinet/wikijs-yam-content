---
title: YAM Rebasing
description: 1 YAM = $1 ???
published: true
date: 2020-08-17T20:09:02.416Z
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

`yamScalingFactor` is the value by which "OG YAM supply" (5,000,000 YAM originally planned for stakedropping, aka `balanceOfUnderlying` in the YAM contract) is multiplied in order to get the YAM balance value that is displayed in wallets, contracts, and other UIs.  

In the contract, this `yamScalingFactor` variable is scaled by x 10**-18: https://etherscan.io/token/0x0e2298E3B3390e3b945a5456fBf59eCc3f55DA16#readContract

In YAM governance, values such as `votes` are denominated in OG supply instead of in wallet balance.

# Scaling Factor History

YAM rebases happen every 12 hours: 8AM and 8PM UTC.  At this time, the `rebase` function on the `YAMRebaser` contract becomes callable by anyone.

> You—yes, YOU—can call the `rebase` function, [but only the first call mined after it becomes active will succeed](https://etherscan.io/address/0x649714bc2fffcb1e65c689b49a10216d4960833d
).
{.is-info}

| Epoch | datetime                     | Balance Scale Factor | = 1 OG YAM | Change |  Rebase TX               |
|-------|------------------------------|----------------------|------------|--------|--------------------------|
| 0     | Aug-12-2020 08:00:00 AM +UTC | 1000000000000000000  | 1   YAM    | ----   | ----                     |
| 1     | Aug-12-2020 08:00:08 PM +UTC | 9307350094489455602  | 9.3 YAM    | +930%  | [0x7b9017ec...][rebase1] |
| 2     | Aug-13-2020 08:00:18 AM +UTC | 18780439270761214101 | 18.7 YAM   | +200%  | [0x32735e9e...][rebase2] |
| 3     | Aug-13-2020 08:00:24 PM +UTC | 17889705531675302598 | 17.9 YAM   | -5%    | [0x527b8a97...][rebase3] |
| 4     | Aug-14-2020 08:07:53 AM +UTC | 16980295531490104432 | 17.0 YAM   | -5%    | [0xae58745c...][rebase4] |
| 5     | Aug-14-2020 08:04:52 PM +UTC | 16411751552705509551 | 16.4 YAM   | -3.5%  | [0x613d23a0...][rebase5] |
| 6     | Aug-15-2020 08:01:45 AM +UTC | 15985697655747854180 | 16.0 YAM   | -2.5%  | [0x4c64faec...][rebase6] |
| 7     | Aug-15-2020 08:00:09 PM +UTC | 15356704803425008450 | 15.4 YAM   | -4%    | [0xabe13f7f...][rebase7] |
| 8     | Aug-16-2020 08:03:42 AM +UTC | 14681935211341898592 | 14.7 YAM   | -4.5%  | [0x3cbae78c...][rebase8] |
| 9     | Aug-16-2020 08:04:03 PM +UTC | 13845372019807670051 | 13.8 YAM   | -5.7%  | [0xab9f2f2e...][rebase9] |
| 10    | Aug-17-2020 08:03:25 AM +UTC | 12955002278062718827 | 13.0 YAM   | -6.5%  | [0x71af3da8...][rebase10] |
| 11    | Aug-17-2020 08:00:00 PM +UTC | 12193451105048975899 | 12.1 YAM   | -6.9%    | [0x3379bb1d...][rebase11] |
| 12    | Aug-18-2020 08:00:00 AM +UTC | TBD | TBD   | TBD  | [...][rebase12] |


[rebase1]: https://etherscan.io/tx/0x7b9017ec92b0200455e5269380195fbecfbf91c8acda30985cc1dc413d215076
[rebase2]: https://etherscan.io/tx/0x32735e9e9aac51739b5725a225be6c7a3851f422be986d0f4f4bc0ec475ee286
[rebase3]: https://etherscan.io/tx/0x527b8a970a53bd46d99d758aa16ff9c2218513b46647a7cfbff72f8a22f8aedc
[rebase4]: https://etherscan.io/tx/0xae58745c11679894bdcbd5b977e864b669148f61b73009f72551c32a07ba9466
[rebase5]: https://etherscan.io/tx/0x613d23a0315b068ac183376fe786188c4c65972970f7d3cdb490eba95eae8549
[rebase6]: https://etherscan.io/tx/0x4c64faeca69106807930badf7801b3db5ffbcbf3212d076bea2b7b1a048eb83b
[rebase7]: https://etherscan.io/tx/0xabe13f7f9a27370c07f1eb711af4b37442df4d4bf0234febefcc5a4c79d043ec
[rebase8]: https://etherscan.io/tx/0x3cbae78cd78fbc7a466ffb3956f3f95928579f40f14fceda978a1c5d81d26a64
[rebase9]: https://etherscan.io/tx/0xab9f2f2e188fc4cd8d0755c2eedc77bb7aab705f5493704576b802617fc583b0
[rebase10]: https://etherscan.io/tx/0x71af3da8a8ca503e1ae68dc708772be623024213572192b7a192504cfdfea620
[rebase11]: https://etherscan.io/tx/0x3379bb1d2fab33b1391f78fac38103de2554da96768cc0046e434a6f13d74262
[rebase12]: #



# How Rebases Are Calculated

The best way to understand the `rebase` calculations is to read the `rebase` code in the `YAMRebaser` contract: [0x649714bc2fffcb1e65c689b49a10216d4960833d][etherscan-rebaser]

Let's look at examples from this code to determine how to calculate how much YAM supply—and therefore wallets and contract balances—will change when a `rebase` occurs.  (Examples here are for if a `rebase` would have been triggered at 2020-08-14 13:45 Pacific Time)

Docstring description of the `rebase` function:
```
* @dev The supply adjustment equals (_totalSupply * DeviationFromTargetRate) / rebaseLag
* Where DeviationFromTargetRate is (MarketOracleRate - targetRate) / targetRate
* and targetRate is 1e18
```

- `targetRate` is the target price of YAMs.  This is $1, expressed as `1000000000000000000` (1x10^18) in `21. targetRate` in the [YAMRebaser contract][etherscan-rebaser].
- `MarketOracleRate` is the YAM TWAP (time-weighted average price) retrieved from the Uniswap YAM:yCRV pool; the current value is displayed by `4. get CurrentTWAP` in the [YAMRebaser contract][etherscan-rebaser].
- `rebaseLag` is 10, which you can see in `14. rebaseLag` in the [YAMRebaser contract][etherscan-rebaser].

At the time of writing this example, this is how the math worked.  First, we calculate `DeviationFromTargetRate` using `targetRate` and `MarketOracleRate`:

```
 559423596560698595 MarketOracleRate (current TWAP from Uniswap)
1000000000000000000 targetRate (target price of $1)

DeviationFromTargetRate = (MarketOracleRate - targetRate) / targetRate
DeviationFromTargetRate = (559423596560698595 - 1000000000000000000) / 1000000000000000000
                        = -0.4405764034393014
```

Now we calculate the change in supply due to the rebase using `deviationFromTargetPrice` and `rebaseLag`:

```

change in supply = _totalSupply * DeviationFromTargetRate) / rebaseLag
change in supply = _totalsupply * (-0.4405764034393014)    / (10)
change in supply = _totalSupply * (-0.04405764034393014)
                 = _totalSupply * -4.4%
```

So if the `rebase` happened at that moment, the total supply—and all YAM balances everywhere in wallets and contracts—would decrease by about 4.4%.



[etherscan-rebaser]: https://etherscan.io/address/0x649714bc2fffcb1e65c689b49a10216d4960833d#readContract

