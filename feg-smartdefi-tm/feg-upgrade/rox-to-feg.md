# ↔️ ROX to FEG

### The Vesting Plan&#x20;

In 2022, we decided to merge ROX into FEG to streamline our ecosystem and enhance value for our investors. All ROX holders have received FEG tokens in exchange. These tokens can be claimed over a 25-month vesting period, with 4% of their holdings released monthly. Investors have the flexibility to claim their 4% monthly or accumulate their claims, for example, over 5 months to claim 20% at once, minimizing gas fees.

{% hint style="warning" %}
Claims are not subject to any taxation however, you DO have to pay the blockchain gas fees to execute transactions, so keep that in mind, especially on ETH
{% endhint %}

### Claims

Latest batch:  claim #4 of 4% was released on September 1st, 2024.

Batches released so far that you can claim in one transaction:   16%

### The ratio of ROX to FEG&#x20;

BSC →   1 ROX = 3,812,101.67910245 FEG\
ETH →   1 ROX = 3,412,864.15305551 FEG\
You can also use [https://calc.fegtoken.com/](https://calc.fegtoken.com/) to make it easier.

### How to upgrade ROX to FEG

<figure><img src="../../.gitbook/assets/ROX to FEG.jpg" alt=""><figcaption></figcaption></figure>

Visit SmartDeFi.com and connect your wallet. Click on the "Upgrader" tab on the FEG page, then select the "ROX Convert" tab. Here, you will see the number of ROX tokens linked to your wallet and the number of new FEG you will receive in exchange.\
To complete the upgrade, click the "Approve" button, then the "Upgrade" button.

### Note you can also Upgrade + Bridge

If you want, you can have your new FEG to be delivered or bridged to another chain, like BASE for example. This means the upgrader will convert your old ROX tokens on the current chain and unlock the new FEG on your chosen chain. \
To start the upgrade process, pick your desired chain, click the "Approve" button, then the "Upgrade" button.

To withdraw your new FEG on the chosen chain, first change the network in your wallet, go to the "Bridge" tab, then the "Withdrawals" tab, and click the "Withdraw" button.

<figure><img src="../../.gitbook/assets/withdraw upgraded FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Remember, you need native coins for gas fees on the origin and destination chains.

Gas fees for bridge use are higher than normal transactions !
{% endhint %}

And that's it! You've successfully upgraded ROX to FEG and bridged to another chain in just a few clicks. It's simple and easy.

### Old ROX addresses

```
ROX on BSC // 0xa3D522c151aD654b36BDFe7a69D0c405193A22F9
```

```
ROX on ETH // 0x378c77C5379cA07BBB5B3506c08a1C769dEC91c2
```

## FAQ

### Are claims automatic or manual?

It is manual, and you need to use the upgrade tool on [SmartDeFi.com](https://smartdefi.com) to claim your FEG.

### How do I receive FEG?

On every claim, you have 3 options to choose from related to where you receive the new FEG:

1. claim FEG in a wallet on the current chain
2. claim FEG in a wallet to the chain of choice (BSC/ETH/BASE)
3. claim and auto-stake on the current chain

### How was the ratio of ROX and FEG calculated?

We established the ratio using the opening prices of FEG and ROX on May 15, 2022. The value of ROX and FEG was calculated by dividing the number of native coins (ETH or BNB) paid by the number of tokens (FEG or ROX) received. To determine how much FEG one ROX yields, we divided the native coin value of one ROX by the native coin value of one FEG. In simple terms, this ratio represents the amount of FEG you could have bought for the same price as one ROX.

BSC Open Transactions\
**ROX**: 0x1a0e998a173ef8b395513f85a44b5abd8db2c9f7a79daf19f477165015843504\
**FEG**: 0x190b55b45916e4c79a98d061d2edd16c8cf67f119fa3544e0273e6f6b6ee1cd0

ETH Open Transactions\
**ROX** 0x883c756fe5be2182b5e45f80286f8d4c7e2eea23eebe1e15ea53d66932aee026\
**FEG**: 0x0f58396870514f4419ed542dfada345b299971a43f186f1bfc6ea8d29c838bd5\
\*  Note: On May 15, ONLY one ROX ETH transaction – Was used as the open price.

### Why use pre-exploit instead of post-exploit values for FEG

Using pre-exploit variables for both tokens was considered the most logical approach, essentially creating a 'snapshot' of market conditions before either exploit occurred. While ROX would have faced the same market conditions as FEG post-exploit, we avoided speculating on price and circulating supply. Instead, we relied on raw data from the blockchain rather than arbitrary figures.

### Why not use ROX and FEG liquidity pools to determine ratio

We chose not to use this method for two primary reasons:

1\.   FEG did not have an asset-backed LP like ROX. While ROX benefited from having both an asset-backed LP and a market LP, FEG only had a market LP. Therefore, using LPs to determine the ratio would have been unfair, as FEG could not leverage the same asset-backing technology that benefited ROX.

2\.   To avoid heavily diluting FEG investors, we considered the total LP for both tokens. The LP for ROX BSC was approximately 2.23 times greater than for FEG BSC, and the LP for FEG ETH was about 1.42 times greater than for ROX ETH. Using these metrics, ROX BSC holders would have owned 69% of the new FEG V2 supply, and ROX ETH holders would have owned 41%. Such a significant ownership discrepancy across the chains would have been unfair to FEG holders and could have put the project at risk.

·         BSC LPs → ROX = 5672 BNB; FEG = 2544 BNB

·         ETH LPs → ROX = 425 ETH; FEG = 604 ETH
