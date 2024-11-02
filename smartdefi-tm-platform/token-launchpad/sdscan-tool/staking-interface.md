# 🟡 Staking - Interface

<mark style="color:orange;">**This page is under development**</mark>

**Available via SDscan - Staking - Interface (after Staking Protocol is launched).**

<details>

<summary>Read</summary>



1. DATA\_READ()
2. SD()
3. \_owner()
4. amountStaked(address)
5. balanceOf(address)
6. boost()
7. boostBacking()
8. burnWDFee()
9. decimals()
10. delay()
11. depositFee()
12. getAllPendingRewardTokenEarned(address)
13. getPaginatedPendingRewardTokenEarned(address,uint256,uint256)
14. getRewardList()
15. getRewardRound(address)
16. getRewardRounds(address,uint256)
17. getRewards(address)
18. getStakeTime(address)
19. getStakers(address)
20. getSyncLevel(address)
21. getTotalRewards(address)
22. getUserRewards(address,address)
23. isLive()
24. isStaker(address)
25. matureDelay()
26. name()
27. ownad()
28. owner()
29. paused()
30. pendingRewardTokenEarned(address,address)
31. rewardAddresses(uint256)
32. rewardLength()
33. sacrificeEnabled()
34. stakeDeployerAddress()
35. stakeLogic()
36. symbol()
37. totalStakedSD()
38. totalSupply()
39. userRewardCheck(address)
40. withdrawalFee()

</details>

<details>

<summary>Write</summary>



1.  addReward(address,uint256) - Addreward is to send rewards (example wBNB) to users as a payout.

    There's 2 ways to addReward.&#x20;

    Use addReward. This updates round and distributes

    Input reward token contract and input amount +18 zeros

    Alternatively, you can send reward to contract via transfer. This will use synclevel to determine when to auto distribute. If synclevel is 10 tokens, once there is over 10 tokens it will distribute on next event that has sync attached. (Like claim reward)


2.  claimAllReward() - Claim rewards - Claims all accumulated rewards.&#x20;

    Note that there is a mandatory 30 days split for rewards (meaning you get 50% of the rewards if you claim or unstake within the first 30 days, after 30 days staying in staking and not claiming you get the other half of the rewards. In other words: If you claimed half you lost another half (gave to others). If you wait till after 30 days to claim you can claim all.
3. claimRewardTokenEarned(address) - claim specific reward (30 days rules applicable)
4. emergencySaveLostTokens(address,address,uint256)
5. renounceOwnership() - rennounce ownership of management rights of the staking protocol (this will remove management rights for staking protocol). Input burn wallet address and confirm transaction.
6. sendReward(address,address,uint256)
7. sendTokens(address,uint256)
8. setBoost(uint256) - enter 10 for 1%, 1 for 0.1% etc. Max is 100% (1000 and below)
9.  setBoostBacking(bool) - If your SD has backing (for example, in wbnb) and your reward is the same (wbnb). Boost backing will take a % of addReward and send to backing. Applicable to SD owners only.

    Enter true for yes boost and false for no boost


10. setBurnWDFee(bool) - BurnWD will burn the deposit or withdraw fee (if fees are set) if burnWDfee is off and deposit or withdraw fee is on it will distribute rewards to stakers.

    Input&#x20;

    true - if you want withdrawal and deposit fees be sent to burn

    false - if you want to redistribute withdrawal/deposit fees to stakers


11. setDelay(uint256) - Delay is the amount of delay if matureDelay is true

    Input format:

    1 for 1 day

    Min 1 day, max is 30 days.

    Older stakers after 30 days can leave even if project owner restarts 30 day counter, the mature delay will apply to new stakers.

    If someone stakes on day 29 they will be able to unstake in 1 day because lock ends for that period.&#x20;


12. setDepositFee(uint256) - Set fee for staking

    Input 10 for 1% format

    Max is 20%\

13. setLogics(address)
14. setMatureDelay(bool) - MatureDelay is when you can exit a stake. Is optional and differs from 30 days split.

    Delay will set the unstaking block, so you can say - stake for X amount of days and you cannot leave. If you don't set a delay, stakers can leave at any moment but they are still under the 30 days reward split rule.

    matureDelay is the bool that is set if you want to enforce a delay.

    Input

    true  - if you want to enforce specific timeframe for how long stakers will not be able to unstake

    false - if you dont want to enforce this\

15. setRewardToken(address,uint256)- Use this to set reward tokens and a threshold (sync level).&#x20;

    SetReward adds a new reward token like adding wbtc.

    Input reward token contract

    Input Sync level +18 zeros (1+18 zeros=1)

    Even if you chose wbnb during deployment (for example), you still need to set the threshold at which the distribution will happen. You can use any erc20/bep20 (or testnet contracts, lp tokens and SD tokens). SetReward is not applicable to native SD token (e.g., you dont need to setRward for SD token itself, only for the additional reward tokens (busd, dai, wbnb etc).

    Example, if you want staking rewards in wbnb be distributed with every 0.5 wbnb added to staking contract:

    Input reward token contract

    0xae13d989daC2f0dEbFf460aC112a837C89BAa7cd

    Input Sync level +17 zeros

    500000000000000000

    Approve transactions.&#x20;

    Min sync level is 1e7 (1+7 zeros = 10000001 which is equivalent to 0.0000001 of a token). \

16. setSacrificeEnabled(bool) - Set True or False to activate it on the owner side to allow users to choose if they want to burn their rewards via Sacrifice function

    _Access: Project Owners_\

17. setSacrificeLevel(uint256) - Only stakers can use this - they can chose % of the rewards they want to send to burn instead.

    Input 100 for 10%, 10 for 1%, 1 for 0.1%. Max is 600 (60%), min is 0. Set Sacrifice needs to be enabled by the project owner first before Stakers can choose the %

    _Access: Stakers_\

18. setStakeLogic()
19. setSyncLevel(address,uint256) - setSyncLevel changes the saved sync level of the reward(the level that it will auto payout)

    Input Reward token address and amount in a format 1+18 zeros&#x20;


20. setWithdrawalFee(uint256) - Set Fee for unstaking

    Input 10 for 1% format

    Max 20%


21. stake(uint256) - Input amount of tokens you want to stake

    1+18 zeros for 1 token


22. start() - Activate your staking for investors be able to start staking
23. syncRewards()
24. transferOwnership(address) - you can transfer management rights for your staking to another wallet. Input address and confirm transaction. Afterwards, token owner will not have access to Staking management if a wallet chosen for ownership transfer will be controled by another person/entity/DAO.
25. withdraw(uint256) - Input amount to unstake&#x20;

    1+18 zeros for 1 tokens

    \


</details>
