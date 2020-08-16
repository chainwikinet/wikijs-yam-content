---
title: YAM Reboot
description: 
published: true
date: 2020-08-16T03:26:27.628Z
tags: 
editor: markdown
---



# #SAVEYAM Vote Delegation

When an issue was found with the [YAM rebasing](/rebase) code, an effort was made to use a YAM governance vote to create an opportunity for YAM v1 to be saved.  In order to perform the governance vote, [the YAM launch team asked all YAM holders to delegate their YAM votes](https://medium.com/@yamfinance/save-yam-245598d81cec) to an address controlled by the launch team ([0x683A78bA1f6b25E29fbBC9Cd1BFA29A51520De84][etherscan-deployer]).  If sufficient votes could be delegated by a deadline a few hours in the future, then the hope was that the YAM launch team could submit and approve a proposal to shut off the faulty rebaser.

## Vote Delegation Success

Sufficient votes WERE delegated and the proposal WAS [submitted][etherscan-propsubmission] and [voted on][etherscan-propvote]:

![yam-vote-delegation-time.png](/yam-vote-delegation-time.png)
*Vote delegation over time. 160,000 votes were needed by the proposal submission deadline, represented by the top right-hand corner of the graph. Votes are denominated in OG YAMs (uninflated by the rebaser), so at the time 1 vote = ~16 YAMs. [source data][votegraph-src]*

## Fix Failure

Unfortunately [the proposal was not able to shut down the rebaser](https://medium.com/@yamfinance/yam-post-rescue-attempt-update-c9c90c05953f) due to an unforeseen interaction between the rebaser and the governance module.  As such, the next rebase happened as scheduled and vast numbers of YAMs were created and transferred into the YAM reserve contract ([0xC53195Bbad57105cc9a4DF752121AfD9C15FBd8f][etherscan-reserve]), permanently breaking YAM governance.


# YAM Reboot

The plan now is to [reboot YAM with a new set of tested and audited contracts](https://medium.com/@yamfinance/yam-migration-plan-dc72ad49aca6).  Existing YAM holders can exchange their current YAM for YAM under the rebooted system.

> When you convert YAM to YAMv2, your balance may be different but you will still own the same proportion of total YAMs!
{.is-info}

The launch team and other community members have advocating for rewarding accounts that delegated votes to help `#saveyam`, even though it was ultimately unsuccessful.  Users who delegated votes had to stop providing liquidity to Uniswap and lost out on potential YAM farming opportunities in the :rainbow: `Eternal Lands` stake pool.  In addition, gas costs at the time were extraordinarily high for the era (>200 gwei), so removing funds from Uniswap and the stakepools and executing the governance delegation function were expensive.

There is broad community agreement and YAM launch team support for a proposal to compensate these delegators for their costs and lost farming opportunities, as an act of goodwill from the entire YAM community for trying to help save the YAM protocol.  It's anticipated that a delegator compensation proposal will be submitted once the migration to the rebooted YAM protocol is complete; approval of this protocol will depend on the votes of YAM holders at tha time.

To aid in this discussion, YAM community member `flygoing` wrote a script that creates a snapshot of delegated balances at the time that the `#saveyam` proposal was submitted: https://github.com/flygoing/yam-snapshots











[etherscan-reserve]: https://etherscan.io/address/0xc53195bbad57105cc9a4df752121afd9c15fbd8f#tokentxns
[etherscan-deployer]: https://etherscan.io/address/0x683a78ba1f6b25e29fbbc9cd1bfa29a51520de84
[etherscan-rebaser]: https://etherscan.io/address/0x649714bc2fffcb1e65c689b49a10216d4960833d

[etherscan-propsubmission]: https://etherscan.io/tx/0x1d64875b24732bc2e8880cd0870ea8e301ddde683ce81fea418e9ab4feea90bb
[etherscan-propvote]: https://etherscan.io/tx/0x9b0fabfdf6f3efde13ef2318c6a416c37b88c9026ca324a54105dc938e9e1f42

[votegraph-src]: https://docs.google.com/spreadsheets/d/1q9crCgp3mkthSAJ5rD_OphLse8hRRpxR7XwrojXqdFQ/

