# 🔶 Token

Use to manage SmartDeFi token.  Accessibly through SDscan - Token - Token contract

<mark style="color:orange;">**This page is under development**</mark>

### **Read**

<details>

<summary>Read commands</summary>



1. BackingLogicAddress() - check Backing Asset contract of the token
2. DATA\_READ()
3. LGE()
4. LGEAddress()
5. LGELive()
6. LPBURN()
7. UNISWAP\_V2\_ROUTER()
8. User(address)
9. WETH()
10. \_UNISWAP\_V2\_ROUTER()
11. allFee(uint256) - need to call each separately. 0-5 Buy/Transfer tax, 6-11 Sell tax

    backing: 0,

    &#x20; burn: 1,

    &#x20; liquidity: 2,

    &#x20; growth: 3,

    &#x20; staking: 4,

    &#x20; reflection: 5,

    backing: 6,

    &#x20; burn: 7,

    &#x20; liquidity: 8,

    &#x20; growth: 9,

    &#x20; staking: 10,

    &#x20; reflection: 11


12. allLastBalance(address)
13. allUser(uint256)
14. allowance(address,address) - check if allowance is granted for expenditure (for example, to check token was approved on being used by additional smart contracts).
15. backingThreshold() - Threshold for Backing Contract to convert tokens to asset-backing that accumulated from Backing Tax&#x20;
16. balance(address,uint256)
17. balanceOf(address) - check balance of the wallet or contract
18. blockNumber(address,uint256)
19. checkLiquidityLock(address) - Check if a liquidity is locked in the SD token contract&#x20;
20. checkWhiteListContract(address) - Check if a contract is in the whitelist
21. decimals() - Check how many decimals a token has
22. frontRun(address,uint256)
23. getAllFee(uint256)
24. isExchange(address) - check if contract is assigned Exhange status (applies tokenomics taxes)
25. lastBalance(address)
26. liqShare()
27. liquidityThreshold() - Threshold for the liquidity contract to convert tokens accumulated from Liquidity tax to the paired asset (if token is paired with WBNB, the contract will convert accumulated tokens to WBNB).
28. liquidityUnlockTime(address) - Check time for liquidity unlock if LP tokens were locked in the SD Lock. Does not refer to the third-party token lockers service providers.
29. name() - token name
30. onlySB()
31. owner() - SD owner
32. sdFeeRecipient()
33. sdOwner() - Check SD token owner
34. sdStake()
35. suggestedAllFee(uint256)
36. suggestedOnlySB()
37. symbol() - get token symbol
38. taxFree(address) - check wallet or contract address if it is TaxFree
39. timeDelay()
40. tokenFromGift(uint256)
41. totalHolders() - get total holders number
42. totalSupply() - get total supply
43. uniswapV2Pair()

</details>

\
**Write**

<details>

<summary>Write commands</summary>

Write commands allow dirrect communication with smart contracts of SmartDeFi token. Some functions are available to only owners and some functions are available to anyone.&#x20;

1. afterConstructor()
2.  approve(address,uint256) - If you want to allow wallet X to move Y amount of SD tokens

    spender (address) - enter the wallet/contract’s address you wish to give approval to

    amount (uint256) - enter desired amount + 18 zeroes


3. endLGE()
4.  extendLiquidityLock(uint256,address) - After you lock your LP in the token’s contract, you can use this function to extend the lock time by however long you want.

    lockDays (uint256) - enter “1” if you want to extend by 1 day. No decimals

    address (address) - enter the LP address of your token

    Min: 1 days

    Max: 9 followed by 70 nines

    Who can access: Project owner\

5.  initialLockLiquidity(uint256,address,uint256) - When you wish to lock your LP tokens directly inside the SD token’s contract you will have to use this function.

    In order to be able to use this function, the first time you use it you’ll need to do an additional approval.

    Example for BNB side: Go to the LP contract on BSCscan on WRITE and on “1. Approve” input this:

    spender (address)  -  input your token's contract address

    value (uint256) -- put a massive number like 1000000000000000000000000000000000000000000000000000000000000000000

    Go to READ on the LP contract and get "balance of" of your wallet and copy that number.

    Now go back to FEGscan on WRITE and on “5. initialLockLiquidity” input like this:

    lockDays (uint256) - enter “1” to lock for 1 day. No decimals.

    address (address) - enter the LP address of your token

    amt (uint256) - enter the amount of LP tokens you wish to lock + 18 zeroes or just paste the number you copied earlier from “balance of” on BSCscan

    Min: 1 days

    Max: 2.74 trevigintillion years (9 followed by 71 nines)

    Access: Project owner


6.  manualBurn(uint256,uint256,uint256) - will be discontinued


7.  removeLiquidity(uint256,address) - Use this function to retrieve your LP tokens from inside the SD token’s contract AFTER the locking time expires.

    You may also use this function to recover ANY tokens, at any time, sent to the token’s contract by other people by mistake.

    amt (uint256) - input amount of tokens you wish to retrieve + 18 zeroes

    address (address) - enter the address of the LP tokens, or the contract address of the tokens you wish to remove if someone sent various tokens by mistake directly to the token contract.

    Access: Project owner


8.  setBackingThreshold(uint256) - The backing contract gathers SD tokens inside from the backing tax and then, when the stored tokens amount limit is reached, it sells said SD tokens on the market in exchange for whatever backing tokens you picked for your project. For example, it sells FEG for wBNB.

    By default the limit is set to 0.01% of the total supply.&#x20;

    amt (uint256) - enter the number of tokens + 18 zeroes

    Access: Project owner


9.  setExchange(address,bool) - If you create a new trading pool pair on another exchange for your SD project, you may use this function in order to enable trading taxes to work properly for that new liquidity pool.&#x20;

    LP (address) - enter the address of the liquidity pool that you want to enable trading taxes for

    adding (bool) - enter TRUE to enable trading taxes&#x20;

    Access: Project owner


10. setFee() - Once the timer limit is reached after the owner of the SD project suggests a new taxation percentage, any user can use this function in order to activate the new taxes percentages for trading. If this function is not used, trading will continue on the old taxes.

    Access: anyone


11. setLGE(address)
12. setLiquidityThreshold(uint256) - The backing contract gathers SD tokens inside from the LP tax and then, when the stored tokens amount limit is reached, it sells said SD tokens on the market in exchange for wBNB, which it will send/inject into the liquidity pool, thus affecting the token-to-wBNB ration and increasing the price of the tokens.

    By default the limit is set to 0.01% of the total supply.&#x20;

    amt (uint256) - enter the desired amount of tokens for the limit + 18 zeroes

    Access: Project owner


13. setNewOwner(address) - When you wish to change the owner of the project you’ll use this function and enter the wallet address to which you wish to be the new owner. You may also renounce ownership of the project by entering the DEAD wallet address (the one with lots of zeroes).

    newOwner (address) - enter the desired wallet address to become the new owner

    Access: Project owner

    \

14. setProtection(uint256)
15. setSDFeeRecipient(address) - You can use this function to change the recipient of the funds gathered during trading by the Development / Marketing Tax. By default the recipient is the wallet address which was used to create the SD project.

    address (address) - enter the wallet address where to receive the funds from Development / Marketing tax

    Access: Project owner\

16. setStakingAddress(address) - used by SmartDeFi Staking Deployer
17. setTaxFreeUser(address,bool) - The owner of the project can pick certain wallets that can trade/move tokens without paying any taxes whatsoever.

    user (address) - enter the wallet address for which you wish to turn ON or OFF the taxes

    adding (bool) - type TRUE to disable all taxes and FALSE to enable all taxes

    Access: Project owner

    \

18. suggestSetFee(uint256\[12],bool) - The owner can edit the trading/transfer taxes for his project at any time after project creation. They can use suggestSetFee to suggest new tax percentages and then wait for 3 days in order to activate  changes  by using 10.setFee.

    feeSet (uint256\[12]) - “10” is 1%, you need to input all 12 taxes, example: “0,1,10,50,70,0,0,10,10,10,10,0” .&#x20;

    onlySellBuy (bool) - set TRUE to enable transfer taxes or FALSE to disable them

    By default, the transfer taxes always copy the “buy” taxes.

    This is the order of the taxes, 0-5 are the “buy” taxes, 6-11 are “sell” taxes:

    &#x20;   \*   fee\[0] = backingFeeBuy

    &#x20;   \*   fee\[1] = burningFeeBuy

    &#x20;   \*   fee\[2] = liquidityFeeBuy

    &#x20;   \*   fee\[3] = growthFeeBuy

    &#x20;   \*   fee\[4] = stakingFeeBuy

    &#x20;   \*   fee\[5] = reflectionFeeBuy

    &#x20;   \*   fee\[6] = backingFeeSell

    &#x20;   \*   fee\[7] = burningFeeSell

    &#x20;   \*   fee\[8] = liquidityFeeSell

    &#x20;   \*   fee\[9] = growthFeeSell

    &#x20;   \*   fee\[10] = stakingFeeSell

    &#x20;   \*   fee\[11] = reflectionFeeSell

    Access: Project owner


19. transfer(address,uint256) - Use the blockchain to send SD tokens from your address to the entered wallet address with the specified amount

    recipient (address) - the target wallet where you want to send tokens to

    amount (uint256) - enter the amount of tokens you wish to send + 18 zeroes

    Access: Project owner


20. transferFrom(address,address,uint256)

</details>
