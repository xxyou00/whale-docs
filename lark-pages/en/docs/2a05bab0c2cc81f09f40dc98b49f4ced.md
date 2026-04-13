---
title: Frequently Asked Questions
slug: 2a05bab0c2cc81f09f40dc98b49f4ced
sidebar_position: 3
---


# Frequently Asked Questions

# FAQs

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The client says the transfer was successful, but I cannot find the corresponding deposit record in the back office. Why?</p>
</div>

A: First, check the system data synchronization status; there might be a 5-10 minute delay. Refresh the page and check again. If the record is still missing, verify whether the client's deposit address has been verified and whitelisted, as the system cannot recognize deposits from addresses that are not on the whitelist. If the issue persists, use the transaction hash (TXID) provided by the client to look up the transaction on a blockchain explorer.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: A deposit record is marked as Abnormal. What are the common causes? How should I handle it?</p>
</div>

A: Common causes include: ① invalid address format (for example, a Bitcoin address filled in an Ethereum address field); ② non-existent transaction hash (TXID) — this may indicate a fraudulent transaction; ③ deposit amount below the platform's minimum threshold. Handle each case as follows: For an invalid address, ask the client to provide a correct address. For a fraudulent transaction, delete the record directly. For an insufficient deposit amount, ask the client to make an additional transfer, or explain to the client why the deposit could not be processed.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q:I clicked Cancel on an unprocessed deposit record, but the system did not respond. Why?</p>
</div>

A: Only records in the Wallet Auth Pending status can be canceled.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: A client requested a refund after a successful deposit, but the operation failed. How should I troubleshoot this?</p>
</div>

A:Work through the following checks in order: ① Confirm that the refund address provided by the client has completed verification. Unverified addresses cannot receive refunds. ② Confirm that the refund network matches the original deposit network. (For example, if the deposit was made via ERC-20, the refund cannot be sent via TRC-20.)

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: During a deposit, the client copied the wrong address and the assets were sent to someone else. What should the client do?</p>
</div>

A: Cryptocurrency transactions are typically irreversible due to the immutable nature of the blockchain. The client should immediately contact the platform's customer service and provide the following information: the sender address, the incorrect recipient address, the transaction hash (TXID), and the time of the transfer. Customer service can then attempt to contact the recipient on the client's behalf. To prevent this from happening again, clients are advised to use QR code scanning instead of manually entering addresses.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: The client selected the correct cryptocurrency, but the transfer did not arrive. Why?</p>
</div>

A: First, check if the network used by the sending platform/wallet matches the network of the target platform/wallet (e.g., if USDT was sent via the ERC-20 network, the destination address must also be an ERC-20 address). A network mismatch will prevent the assets from being credited. Next, use the transaction hash (TXID) to check the transaction status on the relevant blockchain explorer. If the transaction shows as confirmed but the funds have still not been credited, contact the target platform's customer service for further assistance.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Q: A deposit has been in the Confirming status for a long time. Is there a problem?</p>
</div>

A: This is most likely caused by blockchain network congestion or a service fee set too low, causing miners to deprioritize the transaction. The client can use the transaction hash (TXID) to check the current number of confirmations on a blockchain explorer. If the number has not reached the platform's requirement (e.g., 12 confirmations for ERC-20), the client will need to wait. If the service fee is too low, the client should contact the sending platform to check whether transaction acceleration is available.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q:A client forgot to fill in the Tag when transferring XRP, and the assets did not arrive. How should this be handled?</p>
</div>

A: For cryptocurrencies like XRP and XLM, a Tag needs to be entered for funds to be correctly credited. If the client omitted the Tag, the assets will be held temporarily by the platform. In this case, the client should log in to the target platform, find the corresponding deposit record, contact customer service, and provide the transaction hash (TXID) and the missing Tag to request a manual deposit. Remind the client to always copy both the address and the Tag when making future transfers.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Q: Why did the client receive less than the amount sent?</p>
</div>

A: This is an expected result. The difference is due to the blockchain network service fee, which is automatically deducted from the sent amount. If the difference seems unusually large, check whether the sent amount falls below the platform's minimum deposit threshold. Amounts below the threshold may not be credited. In this case, clients can contact customer service to inquire about the possibility of making an additional transfer and whether the two transactions can be combined and deposited together.

