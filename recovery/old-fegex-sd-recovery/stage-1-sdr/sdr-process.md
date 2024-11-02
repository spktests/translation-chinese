# ⚙️ SDR Process

#### No walk in the park

The recovery process is meticulous, involving a sequence of wrapping and unwrapping, converting tokens into their wrapped forms and back again. We've seen it through multiple cycles, adapting it to the unique needs of each project's settings.

#### Liquidity in fBNB and fETH: Wrapping & Unwrapping During the Recovery Process

In SmartDeFi's first iteration, projects have liquidity in fBNB (wrapped Binance Coin) or fETH (wrapped Ethereum).

The recovery process for these projects involves a meticulous sequence of wrapping and unwrapping, which includes:

1. **Wrapping**: This process involves converting BNB or ETH into their wrapped forms (fBNB or fETH).
2. **Unwrapping**: The wrapped tokens (fBNB or fETH) are converted back into their original forms (BNB or ETH).
3. **Multiple Cycles**: The process may require several cycles of wrapping and unwrapping, tailored to the specific needs of each project and the broader ecosystem.

**Additional Aspects of the Recovery Process**

* **Flashloan Fee by PancakeSwap (PCS)**: It's important to note that PancakeSwap collects and keeps a fee for the flashloan, which is not returnable as part of the recovery process.
* **Fee Variability:** The incurred cost ranges from 22% to 28%, including the fWrap taxes incurred during the wrap and unwrap process, distributed as reflections. The cost can increase if re-recovery is necessary (multiple attempts due to the size of the liquidity pool.
* **Routing Decision for Flashloans**: A strategic decision was made to route the flashloans through our FEG/BNB pool rather than opt for one of PancakeSwap's pools, such as BNB/USDT. This choice ensures that the fees imposed by PancakeSwap are partly allocated to our FEG liquidity pool (LP) instead of being entirely directed to PancakeSwap. Notably, executing a flashloan requires approximately 4.5 times more BNB than the liquidity in the pool being recovered. Consequently, as the recovery process progresses, there may be a noticeable increase in the total liquidity of FEG and BNB in our pool, which is a direct outcome of these routing decisions.
* **Fee Allocation**: PancakeSwap adds the partially collected fee to a pre-allocated pool of FEG Tokens at an equal dollar value ratio to the liquidity pool but does not issue LP tokens for this fee. Instead, we must provide FEG Tokens to match the partial fee. This matched amount is then placed into the FEG liquidity pool.

Our team is committed to managing these complexities to ensure the efficient recovery of projects while maintaining the stability and vitality of our ecosystem. We value your ongoing support and are dedicated to transparency as we navigate this intricate recovery process.
