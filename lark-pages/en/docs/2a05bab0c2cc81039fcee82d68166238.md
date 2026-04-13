---
title: System Introduction
slug: 2a05bab0c2cc81039fcee82d68166238
sidebar_position: 0
---


# System Introduction

# I. System Overview

When clients use the Deposit Cryptocurrency and Withdraw Cryptocurrency features, the wallet addresses they use must undergo verification and whitelisting processes.

The wallet address verification workflow may vary depending on the platform and wallet type. The following describes the process using HashKey Exchange as an example.

### Preparations

Confirm that the client's personal wallet supports message signing. Generally, HashKey Exchange does not restrict wallet types. Commonly supported options include software wallets such as MetaMask, Electrum, and MyEtherWallet, as well as hardware wallets such as Ledger Nano S and Trezor.

### Operation steps

1. <b>Trigger Address Verification: </b>When a deposit is initiated, if the client's source address is a personal wallet that has not been verified by HashKey PRO, address verification will be triggered automatically once the client's virtual assets reach the required number of blockchain confirmations.
2. <b>Choose Verification Method: </b>Taking the Metamask wallet as an example, on the Add Deposit Whitelist page, the client should select the MetaMask verification method and click Connect MetaMask.
3. <b>Connect Wallet: </b>A wallet connection interface will pop up. The client should confirm the wallet address to be verified, click Next, and then click Connect<b>.</b>
4. <b>Micropayment Verification:</b> On the Customer Wallet Address page, the client should click Add Verification, accurately fill in information such as the wallet address to be verified and the corresponding cryptocurrency, review the information, and then submit it. Next, the client should log in to their personal cryptocurrency wallet and transfer the specified Verification Amount to the system-generated Verification Address.
5. <b>Complete Verification: </b>Once the micropayment is confirmed, the address is added to the deposit whitelist. For subsequent deposits, the client can directly select this address without verification again.

# II. Operation Instructions

## Permission Preparations

Back office operators log in to WBO and confirm that they have obtained the operation permissions for Cryptocurrency, Channel Custodial Account, and Client Wallet Address. Operators who have not been granted the required permissions should contact the administrator to request access.

## Preparation: Cryptocurrency Data Maintenance (First Step for All Operations)

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: WBO &gt; Service Parameter &gt; Fund Parameter &gt; Cryptocurrency</p>
</div>

Before conducting cryptocurrency deposits/withdrawals and wallet address verification, back office operators must first complete the maintenance of relevant cryptocurrency data:

1. Log in to WBO and go to Service Parameter &gt; Fund Parameter &gt; Cryptocurrency.
2. Click Add or Edit to complete the basic information of the target cryptocurrency (e.g., currency code, name, verification rules, etc.).
3. After verifying that the information is correct, submit it to activate. This ensures subsequent verification and deposit/withdrawal operations can proceed properly.

<img src="/assets/JSOCblFFQoE69ExJrpzjTEbophg.png" src-width="2452" src-height="1180" align="center"/>

## Channel Custodial Account Import

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Channel Custodial Account</p>
</div>

1. Go to VA Clearing Management &gt; Deposit & Withdrawal &gt; Channel Custodial Account.
2. Click Bulk creation and upload the reviewed channel custodial account list (must conform to the system-specified format).
3. After the import is completed, verify that the account information is correct and click Confirm. These accounts are used for automatic assignment before client verification.

<img src="/assets/IVxXb8zUToFpzaxNPC3jLfIcpMh.png" src-width="2480" src-height="1298" align="center"/>

## Verification Record Monitoring

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Client Wallet Address</p>
</div>

1. Enter the Client Wallet Address page to view verification application records for all clients.
2. Supports filtering and searching by criteria such as Verification Status, Created Time, and Client ID. Click on a record to view details (including the assigned custodial account, payment information, verification results, etc.).
3. For records in the Unauthenticated status, operators can assist clients in troubleshooting (for example, verify whether the transfer has been received or whether the addresses match).

<img src="/assets/X7dNb8Z3VoinIixejMpj2wfapve.png" src-width="2446" src-height="1160" align="center"/>

## Whitelisting and Subsequent Management

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Client Wallet Address</p>
</div>

1. After a client's address is verified, the system automatically adds it to the whitelist. Operators can view all whitelisted addresses in the back office.
2. Operators may manage whitelisted address statuses as needed — for example, removing addresses to mitigate exception risks.
3. Operators should regularly export verification and whitelisting records for compliance filing and data archiving.

<img src="/assets/XWJ1bmawzoJ9nExJ2lqj96ekpWb.png" src-width="2464" src-height="1172" align="center"/>

## Precautions

1. Clients must submit their own wallet address for verification. Using another person's address may result in funds not being credited correctly.
2. The funds used for micropayment verification are solely for identity verification purposes. No fees are charged, and there is no need to withdraw these funds separately after verification is complete.
3. Operators should properly keep operation records and transfer receipts generated during the verification process to facilitate future troubleshooting.
4. If a system error occurs — such as a page failing to load or a submission error — refresh the page or try a different browser. If the issue persists, contact the technical support team.
5. Operators shall strictly comply with relevant cryptocurrency business regulations and platform rules. Falsified verifications will result in account restrictions; serious violations may result in termination of services.

