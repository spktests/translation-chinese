# 🪙 启用质押

{% embed url="https://www.youtube.com/watch?v=_UvAYmQXnEc" %}

{% hint style="success" %}
注意：使用 SmartDeFi 质押协议的费用结构：

* 项目所有者启用质押合约时需支付 100 美元的 FEG 代币费用（FEG 费用具体值待宣布）。FEG 代币将在部署过程中被销毁。费用为 100 美元的 FEG 代币，将根据市场价格在部署时确定。
* 质押者进入质押时需支付 1% 的费用。此部分将分配给 FEG 质押者，以扩大持有者名单并增加您项目的曝光率。
{% endhint %}

## **部署质押**

<figure><img src="../../.gitbook/assets/deploy staking UI.jpg" alt=""><figcaption></figcaption></figure>

在您铸造新代币后，您可以为项目启用质押功能，使投资者能够质押他们的代币并从质押税中获得更多的被动奖励。\
\
第一步是为您的质押系统选择名称和符号，然后进行授权，该步骤会以服务费用购买并销毁 X 数量的 FEG 代币 _(最终金额尚未确定)_，然后点击“创建质押”并接受钱包应用的请求。&#x20;

随后，您将进入步骤 2，您会看到多个自定义质押合约的选项。您可以现在深入设置这些选项，也可以在方便时稍后编辑。如果一切设置妥当，您可以点击“启用质押”按钮，为投资者公开启动质押系统。

## 自定义质押合约

SmartDeFi 系统考虑到灵活性，允许您在质押合约发布前后多次编辑选项，使您可以随时根据项目的发展需求和社区的需求自定义质押。

### 存取款费用

<figure><img src="../../.gitbook/assets/deposit and withdrawal fees.jpg" alt=""><figcaption></figcaption></figure>

您可以设置存款或取款时需要支付的税费，这可以是质押或取消质押资金的最高 10%，当然也可以设为 0%。\
注意，例如用户在质押时取款费设定为 2%，即使您之后将其增加*到 10%，系统也会记住该用户的初始税率，因此取款费仍然是 2%。增加的税只适用于新质押用户，旧质押者仍保持原税率。但如果新税率降低*到 1%，那么新旧质押者都适用新税率。&#x20;

### 质押费用分配

<figure><img src="../../.gitbook/assets/set staking fee allocation.jpg" alt=""><figcaption></figcaption></figure>

如果您启用了存取款税，您可以选择如何使用这些收入，可以将其分配给质押者，也可以将其销毁，从而加速您通缩项目的燃烧速率。

### 取消质押延迟

<figure><img src="../../.gitbook/assets/mature unstake delay.jpg" alt=""><figcaption></figcaption></figure>

合约允许您设置用户质押后的 X 天延迟，以便限制他们在质押后的特定时间内不能取消质押，或直接允许用户随意存取。\
首先，您需要点击“启用延迟”按钮，然后选择所需的延迟天数，最后点击“设置延迟”以激活新设置。

### 启用质押奖励燃烧

<figure><img src="../../.gitbook/assets/set reward sacrifice.jpg" alt=""><figcaption></figcaption></figure>

应社区要求，新质押合约引入了质押奖励燃烧功能，旨在帮助减少流通供应。\
启用该选项后，质押者可以选择在取消质押或领取奖励时，从其质押奖励中燃烧一定百分比的奖励。\
默认燃烧率为 0%，用户可自由选择燃烧比例，完全由个人决定是否燃烧。

### 手动注入额外奖励

<figure><img src="../../.gitbook/assets/add reward token staking.jpg" alt=""><figcaption></figcaption></figure>

合约允许您作为项目的开发者手动为质押者提供额外奖励，可直接从个人钱包中注入。\
例如，如果您有来自游戏的 BNB 收入，可将该 BNB 注入质押合约，系统将分配 BNB 给所有质押者，作为他们的质押奖励。\
您还可以设置分配的阈值，规定系统何时开始分发这些奖励。例如，可以设置当注入池中的 BNB 超过 1 个时，才会开始分配奖励，这样您可以分批注入资金，但系统会等到设定的阈值达到后再自动分发。

### 使用奖励代币提升资产支持

如果您的 SD 代币设置的资产支持与奖励代币相同，例如 wBNB，则可以将奖励的一部分分配到代币的资产支持池，而不是分发给质押者。\
此选项称为“SetBoostBacking”，目前可以在 SDscan > Staking > Interface > Write 中找到，为第 9 项。您可以输入 0 到 100% 之间的任意数字，然后点击“写入”按钮以激活更改。
