# 🪙 Enable Staking

{% embed url="https://www.youtube.com/watch?v=_UvAYmQXnEc" %}

{% hint style="success" %}
Note: fee structure to use SmartDeFi Staking Protocol:

* There is a 100$ fee in FEG token that will be required for project owners to have to be able deploy staking contract (FEG fee value to be announced). FEG tokens will be burned during deployment. The cost of 100$ of FEG will be determined during deployment and dependant on the market price.
* There is a 1% fee for token stakers to enter staking. The % will be distributed to FEG stakers which allows expanding the holders list and boost exposure of your project.
{% endhint %}

## **Deploy Staking**

<figure><img src="../../.gitbook/assets/deploy staking UI.jpg" alt=""><figcaption></figcaption></figure>

After you've minted your new tokens you can enable the staking feature for your project, thus allowing your investors to stake their tokens and earn more rewards passively from the staking tax.\
\
First step is to pick a name and ticker for your staking system and then do the approval, which will buy and burn X amount of FEG _(final amount not yet decided)_ as a service fee, then click on "Create Stake" and accept whatever requests your wallet app needs.&#x20;

Afterwards, you will move to step 2 where you should see a multitude of options to customize your staking contract. You can either dive into them and edit now, or you can simply edit them at a later date when convenient to you. If it's all ok for you, you can now proceed to click the "Enable Staking" button in order to launch the staking system publicly for your investors.

## Customize staking contract

The SmartDeFi system was built with customization in mind, as such the system will allow you to edit quite a few options related to your staking contract and you can do that both before and after launching your staking contract, thus giving you the freedom to edit the staking as needed whenever you want and however many times you want, based on the evolving requirements of your project and the needs of your community.

### Deposit and withdrawal fees

<figure><img src="../../.gitbook/assets/deposit and withdrawal fees.jpg" alt=""><figcaption></figcaption></figure>

You may choose to set up a couple taxes that your investors would have to pay when they would deposit funds into staking or when taking out funds. This tax can be up to 10% of the funds users stake or unstake, or you can just leave it at 0 if you wish.\
Note that if for example the withdrawal fee was set at 2% at the moment a user staked, even if you later change the tax and increase\* it to 10%, the system will remember the original taxation level for that particular user, so they will still have a 2% withdrawal fee. Your increased tax will only apply for new users/stakers, not for old stakers. That being said, if your new tax actually lowers\* the tax from 2% to for example 1%, then that new tax applies for both old and new stakers.&#x20;

### Staking fee allocation

<figure><img src="../../.gitbook/assets/set staking fee allocation.jpg" alt=""><figcaption></figcaption></figure>

If you've decided to enable a deposit or withdrawal tax, you can also choose what to use said taxes for and that gives you two options, you can either allocate that income to your stakers or you can burn it, thus increasing the burn rate of your deflationary project.

### Unstake Delay

<figure><img src="../../.gitbook/assets/mature unstake delay.jpg" alt=""><figcaption></figcaption></figure>

The contract allows you to set a custom delay for users so that they cannot unstake for the next X days after they first staked, or you can just leave it as is and people can go in and out as they please.\
First you'll have to click on "enable delay" button and then you can choose the desired number of days to block people from unstaking and finally click on "set delay" to activate the new settings.

### Activate Sacrifice for your Staking

<figure><img src="../../.gitbook/assets/set reward sacrifice.jpg" alt=""><figcaption></figcaption></figure>

The sacrifice feature was introduced in the new Staking contract per community request for those who wish to help with the burn efforts and decrease the circulating token supply.\
When this option is enabled by you the dev, the stakers can choose to burn a custom percentage they choose from their staking rewards at the moment they unstake or claim rewards..\
Sacrifice is set to 0% by default, so that way the users get to decide personally how much they would like to burn, if any at all.

### Additional rewards injected manually

<figure><img src="../../.gitbook/assets/add reward token staking.jpg" alt=""><figcaption></figcaption></figure>

The contract allows you as the project's developer to give your stakers additional rewards, which you can do by injecting them manually from inside your own wallet.\
For example say you have an additional stream income of BNB from a game or whatever, you can take that BNB and inject it into the staking contract which will then split said BNB between all stakers and they will all receive their share of that BNB as staking rewards. \
You may also choose the distribution threshold when the system will start distributing said BNB between your stakers, so for example you can tell the system to only distribute the BNB rewards once you have 1+ BNB injected in the pool, so you can inject funds in smaller batches over time but the system will not auto-distribute until the set threshold is reached.\


### Boost your Asset Backing using the reward tokens

If your SD\_token has the same token set for asset backing and also as an additional reward, for example wBNB, then this option will allow the contract to take a percentage of the additional reward and send that share to the token backing pool instead of sending it as reward for stakers.\
This option is called "SetBoostBacking" and for now it can be found in SDscan > Staking > Interface > Write and in that list it will be option #9. You can input anything between 0 to 100% and then click on the "write" button in order activate the edit.
