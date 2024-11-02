# 🎁 质押

<figure><img src="../../.gitbook/assets/Screenshot_18.png" alt=""><figcaption></figcaption></figure>

### 持有者的被动奖励

加密投资者总是在寻找方法来最大化其持有量并生成被动奖励，而质押协议正是提供了这样的机会。它允许持有者质押其代币并从 PancakeSwap 或 Uniswap 等去中心化交易所的交易量中获得奖励。

### 质押合约功能

<table data-card-size="large" data-column-title-hidden data-view="cards"><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>质押合约自定义</strong></td><td>所有者可以自定义质押选项，例如存款和提取费用、费用分配、解除质押延迟和额外奖励。</td><td></td></tr><tr><td><strong>自动奖励分配</strong></td><td>奖励会自动分配并复利，用户无需手动申领或再投资其收益。</td><td></td></tr><tr><td><strong>可升级合约</strong></td><td>质押合约将被升级，而无需用户和 SD 项目所有者采取行动。</td><td></td></tr><tr><td><strong>奖励来源</strong></td><td>奖励可来自交易，或由所有者手动注入其他代币奖励 <em>（最多 30 种不同的奖励）</em></td><td></td></tr><tr><td><strong>SDSS 代币</strong></td><td>质押后，用户将获得 SD Stake Shares (SDSS) 以表示在质押池中的所有权。为安全起见，SDSS 不可转让。</td><td></td></tr><tr><td><strong>牺牲功能</strong></td><td>用户可以选择在解除质押时燃烧部分质押奖励，以帮助减少流通代币供应。</td><td></td></tr><tr><td>无锁定期的灵活性允许您随时解除质押，或项目开发者可以为其项目选择自定义的锁定期。</td><td></td><td></td></tr><tr><td>开发者可以决定其项目是否需要存款和提取费用，以更好地适应其代币经济学。</td><td></td><td></td></tr></tbody></table>

### **质押奖励来源与分配**

质押奖励来自 SmartDeFi 项目的链上交易活动；它们会自动复利，并随时可供用户提取。\
\
此外，项目所有者可以手动注入其他代币奖励给质押者。\
其他代币奖励将按轮次发放，并受某一累计阈值限制。开发人员可以调整奖励的累积阈值，这可能因不同的奖励类型而异。\
\
例如，如果阈值为 1 wBNB，当奖励池积累至 1 wBNB 时将发放奖励。

{% hint style="warning" %}
在初次质押后的 30 天内解除质押或追加质押将导致 50% 的奖励损失。\
\- 这些被没收的奖励将分配给其他利益相关者。&#x20;
{% endhint %}

### **什么是 SDSS**

质押后，您的 SD 代币将被存入质押合约，您将获得称为 SmartDeFi Stake Shares (SDSS) 的新代币作为回报。这些股份代表您在质押池中的所有权。可以将 SDSS 视为系统出具的收据，以确认您已成功质押。您需要展示该收据，以便系统允许您解除质押并归还您的 SD 代币。

* SDSS 不是 1:1 比例
* SDSS 随每次赚取的代币奖励更新
* 总 SDSS / 总 SD = 比例
* SDSS 无法转移到其他钱包。

### 可选“牺牲”功能

新的质押合约应社区要求引入了牺牲功能，适用于那些希望帮助燃烧和减少流通代币供应的人。

在解除质押时，质押者可以燃烧其质押奖励的指定百分比，从而有效地将其从流通供应中移除。

要激活此功能，您必须指定要牺牲的百分比和要解除质押的数量。

{% hint style="success" %}
在解除质押之前，您可以随时通过在牺牲设置中将其设置为 0% 来关闭牺牲功能。
{% endhint %}
