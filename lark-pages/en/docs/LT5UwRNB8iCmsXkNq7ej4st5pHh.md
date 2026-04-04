---
title: Frequently Asked Questions
slug: 2a05bab0c2cc81a0b6d2c2008e1e6d28
sidebar_position: 3
---


# Frequently Asked Questions

# FAQs

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The client receives an &quot;insufficient balance&quot; error when submitting a withdrawal application, even though the account appears to have enough funds. Why?</p>
</div>

A: There is a difference between the available balance and the frozen balance. If assets are in a T+1 lock-up period (e.g., cryptocurrency purchased within the last 24 hours), involved in unredeemed financial products, or tied to open trade orders, they will show as frozen. Only the available balance can be used for withdrawal. Additionally, the applicable service fee should be considered. If a client enters a withdrawal amount equal to their full available balance, the transaction may fail because there are insufficient funds to cover the service fee after deduction. Clients are advised to leave a small reserve to cover the service fee.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: Why is a newly registered account unable to initiate a cryptocurrency withdrawal?</p>
</div>

A: For regulatory compliance, platforms typically impose a risk control observation period for new accounts, usually lasting 7 to 10 calendar days. Cryptocurrency purchased during this period cannot be withdrawn until the observation period has ended. In addition, accounts that have not completed advanced KYC verification may have withdrawal function restricted. Clients can unlock this feature by completing identity verification (for example, by submitting a passport and proof of address).

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: What happens if the client omits or incorrectly enters the Memo/Tag when withdrawing? What steps should they take?</p>
</div>

A: For cryptocurrencies like XRP, XLM, and EOS, a Memo/Tag needs to be entered for funds to be correctly credited. If the client omitted the Memo/Tag or provided an incorrect one, the assets will be held temporarily by the platform (will not be lost). The client should contact the recipient platform's customer service, provide the transaction hash (TXID), withdrawal address, and correct Memo/Tag, and request a manual deposit. Remind the client to copy both the address and Memo/Tag and double-check to avoid errors.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: After the client clicks Confirm Withdrawal, the page freezes, and no transaction hash (TXID) is generated. Should the client resubmit the application?</p>
</div>

A: Do not resubmit. An unresponsive page is most likely caused by a network delay or a temporary system issue, and the application may already have been received with a status of Pending Submission. The client can go to Withdrawal &gt; Withdrawal Application to check the status. If the status is Pending Submission, the client should wait for processing. If no status is displayed after an extended period, the client should log out and back in, or clear the browser cache, and check again. Only if the client can confirm that the request was not submitted at all should they resubmit the application.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The withdrawal status shows Completed, but the recipient has not received the funds. How should I resolve this?</p>
</div>

A: Handle this issue in three steps: ① Use the transaction hash (TXID) to check on the corresponding blockchain explorer to confirm that it has received the required number of on-chain confirmations (e.g., BTC requires 6 confirmations). ② If the blockchain shows the transaction is successful, contact the receiving platform's customer service, provide the TXID and receiving address, and check whether the delay is due to a synchronization issue on their system. ③ If the assets have been returned (i.e., the blockchain shows the transaction as "Failed"), the funds will be automatically credited back to the original withdrawal account. In this case, the client should allow 1 to 3 hours for the funds to be returned.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The amount received is significantly less than the amount withdrawn. Was the difference deducted by the platform?</p>
</div>

A: The shortfall is typically attributable to two factors: ① Network service fee (e.g., miner fee), charged by the blockchain network and automatically deducted from the withdrawal amount. The fee rate fluctuates with network congestion at the time of the transaction. ② The receiving platform's deposit threshold. If the withdrawal amount falls below the receiving platform's minimum deposit requirement (e.g., ≥ 0.001 BTC), the transaction may be rejected and returned, incurring an additional service fee. Clients are advised to review the fee structure and minimum deposit requirements of the receiving platform before initiating a withdrawal.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The client accidentally sent ETH to a BTC address, or sent USDT on the ERC-20 network to a TRC-20 address. Can the assets be recovered?</p>
</div>

A: Such cross-chain or cross-token transfers are incompatible due to differences in address formats. In most cases, the assets will become permanently inaccessible and cannot be recovered automatically. However, the client may attempt the following: ① Contact the receiving platform’s customer service, provide the transaction hash (TXID) and transfer proof, explain the error, and inquire whether a manual return is possible. Note that the likelihood of recovery through this route is generally low. ② If the funds were sent to an incorrect personal address and the client holds the private key for that address, they may be able to import the private key into a compatible wallet on the corresponding network to retrieve the assets. To prevent such errors from occurring, clients are advised to use QR code scanning rather than manually entering addresses, and to verify at least the first and last five characters of the address before confirming any transfer.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The WBO work order shows Approved, but no on-chain transaction was triggered. What could be the reason?</p>
</div>

A: This may be due to insufficient balance in the platform’s withdrawal hot wallet. In this case, the system will initiate a transfer from the cold wallet to the hot wallet, which typically takes 15 to 30 minutes to complete. In addition, if the relevant blockchain network is experiencing extreme volatility (for example, a sudden spike in gas fees), the system will temporarily pause transaction broadcasting and wait for network conditions to stabilize before automatically resuming execution. The client can check the hot wallet balance on the platform's Wallet Status page or contact customer service to inquire about the transaction queue status.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q:Can the withdrawal service fee be adjusted manually? Why is the service fee sometimes exceptionally high?</p>
</div>

A: Some platforms support manual adjustment (e.g., the Advanced options on Coinbase Pro). Setting a higher service fee gives the transaction greater priority for inclusion by miners, which can result in faster processing. A sudden sharp increase in fees is usually caused by blockchain network congestion (e.g., ETH gas fees exceeding 150 Gwei). Under these conditions, the platform dynamically raises the default fee to improve the likelihood of successful transactions. To minimize fees, clients are advised to avoid initiating withdrawals during peak network hours (typically UTC daytime) or switch to a Layer 2 network such as Arbitrum.

