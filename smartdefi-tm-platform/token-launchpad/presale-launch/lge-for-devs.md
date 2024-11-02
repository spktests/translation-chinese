# 👤 LGE for Devs

{% hint style="info" %}
This page is being updated with the latest implementations&#x20;
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=7SpIEcXtqYY" %}

Suppose you don't have the private funds to add liquidity to your SmartDeFi project, in that case, you can gather liquidity from investors using the Liquidity Generation Event system, LGE for short, or known as _"presale"_ for the simple folks as myself.

## Step 1 - Deploy the LGE

<figure><img src="../../../.gitbook/assets/deploy LGE jan.jpg" alt=""><figcaption></figcaption></figure>

As you've noticed, the LGE Deployer has quite a few options for you to customize, so let's quickly go through each of them:

**• Tokens for LGE**  (SD-tokens amount)\
Here, you can decide how much of your SD-token supply you wish to give towards the presale. It is advised you place 100% of the supply.

**• Rate**  (SD-tokens per BNB)\
The number of tokens you choose here will decide the price people buy your token for during the presale and immediately after.\
\- Note: Whatever setting you pick in the "Backing share" field will also affect the price.

**• Max buy**  (BNB/ETH)\
The maximum number of BNB/ETH investors can use to buy into your presale.

**• Start date and time** \
You may pick an exact day and hour when the presale can activate and run.

**• Duration** (Days)\
The number of days you wish your presale to run before it closes automatically.

**• Vesting delay**  (Days)\
The system can release locked liquidity in batches, and you can decide how many days to have between each batch.

**• Vesting rate**  (%)\
You can decide how much of the locked liquidity to release during each unlock batch phase.

**• Backing share** (%)\
When the LGE finishes the presale, a percentage of the gathered BNB/ETH can be injected into asset backing to create a more stable token. It is advised to place 50% so that once released, the token's price will initially be similar to its asset backing value.

**• Dev Share** (%)\
The system can give the SD owner a percentage of the liquidity and vest it, as it's also vested for regular investors. The project can use this share for whatever they need, like marketing, CEX listings, etc.

**• FEG share** (%)\
The system will place the gathered BNB/ETH into two liquidity pools, one for SD/BNB and one for SD/FEG. You may choose how to split these two liquidity pools. This also insures that your investors have an opportunity for arbitrage right out of the gate, so more income for you via taxes.

Now that you've picked all your preferred settings for the LGE, it is time to hit the "_Approve_" button at the bottom, accept whatever approvals you receive from your wallet app, and cover the required blockchain gas fees for transaction execution.\
\
Once that is done, you'll see a new button called "_Deploy_" click it and accept the wallet approvals, and then that's it, your LGE is now deployed and ready to roll based on the settings you picked.

### 1.1 Edit the LGE before it activates

<figure><img src="../../../.gitbook/assets/edit presale after.jpg" alt=""><figcaption></figcaption></figure>

Once you create the presale, you have a grace period where you can still edit it before it actually starts. \
In your token's dashboard click on "Edit LGE" and that will open a new popup menu where you'll notice all the settings you just made earlier and also next to each there will be an "edit" button, click it and this will allow you to edit whatever you need.\
Remember that you cannot perform any edits once the presale has started and is live.

### 1.2 Whitelisting addresses for presale

<figure><img src="../../../.gitbook/assets/whitelist address.jpg" alt=""><figcaption></figcaption></figure>

When you edit the presale, before it goes live, you have the option to add a whitelist to your presale, meaning you can add a number of wallet addresses that are VIPs and who will be a secured spot in the presale once it goes live, meaning the presale will be locked to the general public, until the VIPs buy into the presale. \
Every VIP can only invest into the presale the same amount of ETH/BNB as any other user can, so the max amount has the same cap for everyone.\
You will first need to enable the whitelist, then you add the addresses you wish and finally you click on the "whitelist addresses" button.\
After all the whitelisted addresses buy into the presale, then the presale will automatically open up to the general public and everyone can start investing.\
The presale will be locked towards the public until ALL the whitelisted addresses buy into the presale.\
You as the dev can also remove people from the whitelist, if you need to. You can also disable the whitelist entirely if you decide so, some time after you've already enabled it, if for example one of the whitelisted wallets goes inactive and doesn't buy into the presale, thus keeping the presale locked for the average users. So you have the option to boot people from the whitelist or disable it entirely, if you have such problems with one or more users.

## Step 2 - Ending the LGE and launching project

If you as the DEV don't open up trading within 72 hours after LGE ends, then your investors will be able to cancel their participation into the LGE and can recover their invested funds.

If the 72h limit passes and people start withdrawing their money from the presale pool and if amount falls below softcap, the DEV will still be able to launch the project for trading.

The presale can be ended in 3 ways:

### 2.1 Presale sold out and Hardcap was reached

If you managed to gather all the BNB you set out to raise, then your presale will end the moment that hardcap is reached, regardless if this happens barely 1 day after the presale started and your initial time limit was set for 90 days.\
Once the presale end, you as the DEV will need to manually open up the trading via our UI, at which point the system automatically sets up your liquidity pools on Pancakeswap for BNB or on Uniswap for ETH and BASE.\
After that, you or your investors will need to go to the presale's page on FEGex and click on "Enable shares" button so that your investors can start claiming their shares based on your set schedule.

### 2.2 Presale ends and only Softcap is reached

<figure><img src="../../../.gitbook/assets/closed with softcap (1).jpg" alt=""><figcaption></figcaption></figure>

Once the presale's time limit is reached and it has managed to gather the amount needed for softcap, it is considered the presale is successful and will be placed in the "Completed" subcategory.\
At this point anyone (investor or not) can come and click on "Force end presale".\
The system automatically sets up your liquidity pools on Pancakeswap for BNB or on Uniswap for ETH and BASE.\
After that, you or your investors will need to go to the presale's page on FEGex and click on "Enable shares" button so that your investors can start claiming their shares based on your set schedule.

### 2.3 Presale ends but Softcap is NOT reached

<figure><img src="../../../.gitbook/assets/presale failed (1).jpg" alt=""><figcaption></figcaption></figure>

The presale will automatically be moved in the "Failed" subcategory if your time limit has reached but you did not managed to gather enough funds for softcap.\
At this point any investor can click on the "Abort presale" button and then the "Exit presale" button, clicking this will cause your presale funds to return back into your wallet, in the form of wrapped BNB/ETH.

### 2.4 Special conditions for presale end

After a presale ends, the DEV has a grace period of 72h to launch the trading of his project, otherwise if they don't, after that point the investors can come and start withdrawing their investment.

If softcap/hardcap is reached but dev doesn't deploy trading after said 72h, if most investors withdraw their money and the gathered funds fall below softcap level (but non zero) the dev can still deploy the presale with remaining funds.

If softcap/hardcap reached but then project didn't launch and everyone left (no funds remaining), the dev can later use endLGE and abortLGE and relaunch a new presale with new settings.

If softcap is not reached, the dev can use abortLGE and create a new LGE with new settings.

## EXAMPLE

Let's say you just made a project with 100,000 tokens and you placed all of them into the presale.

Say you have a hardcap of 1000 BNB. The first thing you need to figure out is the asset backing share, for this example let's say 35%. \
35% out of 1,000 = 350 BNB goes to asset backing. \
So 1,000-350= 650 BNB, this is how much will be left to go into LP.

Now the second part of this math operation begins. \
This remaining 650 BNB will be split among the BNB pool and FEG pool. \
Let's say FEG will have a share of 30%, which automatically means the BNB pool will be 70%. \
So 30% out of 650 = 195 BNB, this is how much BNB will be used to buy FEG and set up the SD/FEG pool. \
650-195= 455 BNB, this is how much BNB will be in the SD/BNB pool.

Now for the last part. \
Say you want a 5% dev share for the project. This means that the dev will receive 5% of the SD/FEG pool and 5% of the SD/BNB pool. \
So the dev will receive:\
\- 22.75 BNB worth of SD/BNB vested LP (455 \* 5%)\
\- 9.75 BNB worth of SD/FEG vested LP (195 \* 5%) \
These numbers are valid right at the moment the presale ends. After that trading will begin and when the liquidity pool increases the $ value of the 5% dev share increases too.

## DEV share

You as the developer of your project have the option to activate a DEV share when you set up the LGE that can go up to 50% of the total BNB gathered in the presale. \
After the presale ends you'll be entitled to claim your shares on the same schedule as the rest of the investors, with a single exception. \
Unlike the normal investors, you as the dev can claim a larger first vested share. The formula for the first vested share is amt \* (51 - devshare) / 10. The "amt" is what everyone gets from the vesting schedule at the start, ensuring everyone has a fair beginning.\
This means that the smaller your DEV share % is, the larger your first vested claim can be, so if for example your DEV share is 20%, the formula is (51-20)/10 = 3.1x which means your vesting rate will be 3.1 times larger for you, on first claim only, when compared to the rest of the investors. \
This is set up like this to help new projects in case they need funds early on for various tasks like paying for a CEX, hiring more DEVs, paying for marketing and so on.&#x20;
