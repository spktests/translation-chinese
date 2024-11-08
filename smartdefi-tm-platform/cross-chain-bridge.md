# ⛓️ 跨链桥

<figure><img src="../.gitbook/assets/Screenshot_14 (1).png" alt=""><figcaption></figcaption></figure>

介绍 SmartDeFi 链上跨链桥，这是一项为所有从 SmartDeFi Token Launchpad 上推出的项目提供的革命性功能。

该跨链桥通过链上无缝的不同 EVM 区块链之间的互操作性打开了无限可能，使用户在管理其代币时享有前所未有的灵活性、套利机会和可访问性。

加入我们，共同迈向更加互联和去中心化的生态系统。

### 工作原理

<figure><img src="../.gitbook/assets/bridge 1 FEG base to bnb.jpg" alt=""><figcaption></figcaption></figure>

前往 [SmartDeFi.com](https://smartdefi.com)，连接您的钱包，选择您希望跨链的代币，然后点击“Bridge”标签。

此时，您可以选择您希望跨链的目标链。接下来，输入您希望从链 X 到链 Y 的代币数量。最后，点击“Approve”按钮，然后点击“Bridge”按钮以执行实际的跨链交易。

接下来切换您的钱包网络到您发送代币的链上，然后确保在“Bridge”标签的“Withdrawals”标签下操作。确认显示的信息正确后，点击“Withdraw”按钮。

{% hint style="success" %}
请记住，您需要在源链和目标链上都有足够的原生代币用于支付 gas 费。

跨链桥的交易费用比普通交易更高！
{% endhint %}

就这样，您可以通过几次点击将代币跨链到另一条链上，简单且方便。

<figure><img src="../.gitbook/assets/withdraw bridge 1FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
跨链桥每 15 分钟只能进行一次跨链操作。

用户有 30 天的时间从 SmartBridge 领取资产。

未领取的资产将被永久丢失。
{% endhint %}

### 常见问题解答

1. **谁可以启动跨链桥的创建？**
   * 只有 SmartDeFi 代币智能合约的所有者可以启动跨链桥的创建。这确保了跨链的授权访问以及所有者钱包的验证。

2. **代币供应可以在多个链上分配吗？**
   * 是的，可以通过将代币分配到跨链桥，将总供应分配到多个链上。用户可以从原始链的供应中将代币跨链到新的链上，同时保持总供应的完整性。

3. **跨链的供应转移如何工作？**
   * 用户将代币存入跨链桥，在当前链上锁定代币，并选择要提取的目标链。此过程会将代币释放到所选链的流通中。

4. **外部合约能与跨链桥交互吗？**
   * 只有经过验证的源地址和链上的经过验证的合约可以与跨链桥交互（除了用户功能以外）。该安全措施确保了对跨链桥功能的控制访问。

5. **费用是多少？**
   * 跨链桥的基本费用为 1 美元，但您的操作成本会更高，因为跨链桥需要在两个链上同时执行多个合约操作，因此会产生额外的 gas 费用。例如，一笔 BNB 存款和 BASE 提款的跨链交易可能总共花费 9 美元，但这些费用将根据网络当时的使用情况有所不同。
