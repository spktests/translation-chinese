# ⛓️ Cross-chain Bridge

<figure><img src="../.gitbook/assets/Screenshot_14 (1).png" alt=""><figcaption></figcaption></figure>

Introducing the SmartDeFi On-Chain Cross-Chain Bridge, a revolutionary feature available for all projects launched from the SmartDeFi Token Launchpad.&#x20;

The Bridge opens up a world of possibilities with seamless interoperability between different EVM blockchains entirely on the chain, where users can now enjoy unparalleled flexibility, arbitrage and accessibility when managing their tokens.&#x20;

Join us on this exciting journey towards a more interconnected and decentralized ecosystem.

### How It Works

<figure><img src="../.gitbook/assets/bridge 1 FEG base to bnb.jpg" alt=""><figcaption></figcaption></figure>

Head over to [SmartDeFi.com](https://smartdefi.com), connect your wallet, pick the token you wish to bridge and then click on the "Bridge" tab.&#x20;

At this point you will be given the opportunity to choose which chain you wish to bridge to, the next step being that you need to input the amount of tokens to bridge from chain X to chain Y. Lastly You will need to click on the "Approve" button and then on "Bridge" button in order to perform the actual bridging transaction.

Now all that is left to do is switch your wallet's network to the chain where you sent the tokens to, then make sure you're on "Bridge" tab and on "Withdrawals" tab. Check to make sure all the information shown is correct and then click the "Withdraw" button.&#x20;

{% hint style="success" %}
Remember you need native coins for gas fees on both the origin and destination chains.

Gas fees for bridge use are higher than normal transactions !
{% endhint %}

And that's it, you've bridged your tokens to another chain in a few clicks, simple and easy.

<figure><img src="../.gitbook/assets/withdraw bridge 1FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The Bridge is limited to one bridging instance every 15 minutes&#x20;

The user has up to 30 days to claim assets from the SmartBridge&#x20;

Unclaimed assets will be forfeit forever
{% endhint %}

### FAQ

1. **Who Can Initiate Bridge Creation?**
   * Only the owner of the SmartDeFi token's smart contract can initiate bridge creation. This ensures authorized access and owner wallet verification across chains.
2. **Can Token Supply Be Distributed Across Multiple Chains?**
   * Yes, the total supply can be distributed across multiple chains by allocating it to the bridge. Tokens from the originating chain's supply can then be bridged to new chains, maintaining the integrity of the overall supply.
3. **How Does Supply Transfer Work Across Chains?**
   * Users deposit tokens into the bridge, locking them on the current chain and selecting the destination chain for withdrawal. This process releases the tokens into circulation on the selected chain.
4. **Can Outside Contracts Interact with the Bridge?**
   * Only verified source addresses on verified chains can interact with the bridge beyond user functions. This security measure ensures controlled access to bridge functionalities.
5. **What does it cost?**
   * The bridge has a 1$ flat fee but your operation will cost more because the Bridge requires multiple contract executions on 2 chains at the same time, which means extra costs in gas fees; for example a BNB deposit and BASE withdrawal bridge could cost 9$ in all, but these costs will vary for you depending on network usage at the time
