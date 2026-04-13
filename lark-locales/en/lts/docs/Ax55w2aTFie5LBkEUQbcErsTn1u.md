---
title: System Introduction
slug: Ax55w2aTFie5LBkEUQbcErsTn1u
sidebar_position: 1
---


# System Overview

# I. System Overview

Withdrawal refers to the operation by which an investor transfers funds from their securities account. The withdrawal feature allows investors to transfer funds from their securities accounts to their bank accounts or other designated accounts.

The Whale system includes features for processing withdrawal requests, withdrawal handling, reconciliation, separate handling of withdrawal exceptions, and withdrawal record inquiries. In accordance with regulatory and risk-control requirements, the system is designed around a multi-role, workflow-based architecture that balances operational efficiency with financial risk mitigation.

The overall business process is as follows:

<img src="/assets/BzcYwkSRChvaCgbfqtijYLoRp3c-board.jpeg"/>

# II. Operation Instruction

# Withdrawal Configuration

## Fund Parameter Configuration

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Fund Parameter &gt; Company Bank Account</p>
</div>

<img src="/assets/AMzBba2IwoqMPux4ek2jwmsnple.png" src-width="2942" src-height="1320" align="center"/>

- Click Create to open the configuration page and add the relevant withdrawal channel information. A withdrawal channel is defined as the combination of the broker's payment bank account and withdrawal method, for example, ICBC Asia 001 — Cheque Transfer.

<img src="/assets/TJvdbxGcmoRLyQxpa6xjwH4Qp8v.png" src-width="3002" src-height="1332" align="center"/>

1. Enable the withdrawal function for the currency

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Fund Parameter &gt; Currency Setup</p>
</div>

<img src="/assets/Hx2AbhWoBoESrjxhA0bjb2L7ppc.png" src-width="2956" src-height="1326" align="center"/>

- Click Add to open the configuration page and select Yes for the Withdrawal Function option.

<img src="/assets/QK4KbXZbioHgvHxnGkGjxTYepnf.png" src-width="2912" src-height="1338" align="center"/>

## Automatic Withdrawal Rules

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Withdrawal Rules</p>
</div>

On this page, the operator can configure the withdrawal rules, which defines whether the batch withdrawals are processed automatically or manually. The rules also specify single-transaction withdrawal limits, service windows, and supported client banks.

The following withdrawal policies are supported: Real Time Payment Of Single Order, Manual Review Of Timed Packing, Manual Packing, and Batch Auto.

<img src="/assets/EegEbh072owR1ixmv3Yj8zr3pOg.png" src-width="2956" src-height="1312" align="center"/>

Operation button descriptions:

- Add: Create an automatic withdrawal rule according to the broker's withdrawal channels.
- Edit: Modify an existing automatic withdrawal rule.
- Delete: Remove an existing automatic withdrawal rule.

## Daily Limits and Change Log

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Daily Limits</p>
</div>

As certain withdrawal channels may be subject to daily limits, a daily limit monitoring and management mechanism is in place to help minimize withdrawal exceptions.

<img src="/assets/EZZTb00GvoYiByxb7zajcAv2pkz.png" src-width="2986" src-height="760" align="center"/>

Operation button descriptions:

- Add: Configure a daily limit for a withdrawal bank.
- Edit: Modify an existing daily limit.
- Delete: Remove an existing daily limit.
- Adjust: Increase or decrease the daily limit for a withdrawal bank.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Daily Limit Changes</p>
</div>

This page provides a full history of changes made to the withdrawal bank's daily limits.

<img src="/assets/G6AvbXO3Qo6ZcLxGjA0jWv2Qpvd.png" src-width="2938" src-height="1320" align="center"/>

When the remaining balance of the daily limit falls to the alert threshold, the system will automatically send a message alert.

## Withdrawal Interception

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Balance Blocking Rules</p>
</div>

This feature currently applies to withdrawal operations. When a withdrawal is being processed, the system queries the balance of the withdrawal bank selected by the finance team and compares it against the requested withdrawal amount. If the available balance is insufficient to cover the withdrawal, the transaction is automatically intercepted and held for manual review by the finance team.

<img src="/assets/SLWrbvVyVor5B9xKRDej1z2Npuc.png" src-width="2938" src-height="1360" align="center"/>

Operation button descriptions:

- Edit: Modify the alert threshold and the interception threshold for a balance inquiry record of a bank integrated via API.
- Enable: Activate a balance inquiry record of a bank integrated via API.
- Disable: Deactivate a balance inquiry record of a bank integrated via API.

When the bank balance falls to the alert threshold, the system will automatically send a warning notification.

When the bank balance falls to the interception threshold, the system will automatically intercept the affected withdrawals and issue an alert.

## Automatic Review Rules

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Automatic Review Rules</p>
</div>

Operators can configure whether a client's withdrawal application requires manual back-office review in this tab. The following review rules are supported: manual approval with a work order, manual approval without a work order, automatic submission, and automatic rejection.

<img src="/assets/V9QBb2BvPoOiESxdAOMj2fv4pdc.png" src-width="2980" src-height="1182" align="center"/>

Operation button descriptions:

- Create: Set up a new automatic review rule as required.
- Edit: Modify an existing automatic review rule.
- Enable: Activate an existing automatic review rule.
- Disable: Deactivate an existing automatic review rule.

## Additional Settings

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; More settings</p>
</div>

Operators can configure whether the Direct billing operation (located under Cash Management &gt; Withdrawals &gt; Withdrawal - Pending) requires work order approval upon submission in this tab.

<img src="/assets/AZZibyk3xorZ7Ex05MtjAqB7pPb.png" src-width="2982" src-height="748" align="center"/>

## Withdrawal Parameters

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Withdrawal Rules Management &gt; Withdrawal Configuration</p>
</div>

Operators can configure withdrawal parameters such as estimated arrival time and estimated fees on this page, according to the client's withdrawal bank.

<img src="/assets/VaLWbtVMYo9Q5mxr3b8jl2sTpvd.png" src-width="2972" src-height="958" align="center"/>

Operation button descriptions:

- Add: Create a set of withdrawal parameter as required.
- Edit: Edit existing withdrawal parameters.
- Copy: Create a new entry quickly by copying an existing set of withdrawal parameters.

# Withdrawal Operations

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Navigation: Cash Management &gt; Withdrawals</p>
</div>

## Withdrawal Application

A withdrawal application is submitted by the client and includes four main elements: currency, requested amount, beneficiary bank card, and reSets. Back-office operators can manually assist clients with withdrawal submissions, and may also reject or submit a client's application for approval.

- Manual Withdrawal

This feature applies when a client contacts back office operators to request a manual withdrawal. The operator must enter the following information in sequence: currency, requested amount, withdrawal fee, beneficiary bank card, and reSets. If the client has supporting documentation for the withdrawal, this can also be uploaded to the system.

<img src="/assets/DaM6blbDUo9ZX8xIPktj4vvMphc.png" src-width="1204" src-height="3012" align="center"/>

- Submit (batch operation supported): Once the operator has completed a preliminary review and confirmed that the application contains no issues, click Submit to forward the application to the next-stage operator for further review and processing.
- Reject (batch operation supported): If the withdrawal application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Reject.
- Delete: If the withdrawal application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Delete to remove the target record.
- Edit: If an issue is found with a client's withdrawal application before submission for approval, the operator can click Edit to correct it after confirming with the client. Modifications require work order approval; changes take effect after approval.
    - Editable fields: Amount Requested, Handling Fees, Beneficiary Bank Card, Back Office's ReSets, and Upload File.
    <img src="/assets/Z3hbbHY4koTNmKxXzXkjO1OIpEE.png" src-width="2910" src-height="1278"/>
    <img src="/assets/AmAXbeFeyohj1HxUPIDjcx3dpHg.png" src-width="2440" src-height="1194" align="center"/>

## Withdrawal Processing

Once the initial reviewer submits a withdrawal application, the reviewing operator must proceed with withdrawal processing. Two processing methods are available: Direct Withdrawal and Batch Submission for Review.

- Direct Withdrawal
    <img src="/assets/CVy9b3yPwowEzOxMT7tj84egpsd.png" src-width="2938" src-height="1316" align="center"/>
    <img src="/assets/IWFIb2zybohNVWxoPkJjsAIGp8e.png" src-width="2972" src-height="1332" align="center"/>
    <img src="/assets/H2aPbViWwozchNx4jGNjD33Wpkd.png" src-width="2958" src-height="1250" align="center"/>
    <img src="/assets/UQ62b72uwoB0OgxMzDHjxBoJp2e.png" src-width="3054" src-height="1387" align="center"/>
    - Select the target record and click Direct billing in the Action column.
    - In the pop-up window, enter the bank name, bank account, and channel information. Bank statement details may also be included in the Withdrawal Details field.
    - Click Submit for approval. The record will move to the Withdrawal Directly Pending page, where the reviewer must complete work order approval. Once approved, the withdrawal is complete.

- Batch Submission for Review
    <img src="/assets/ZGEib6cepoeq9xxRwfjj3VS4p9d.png" src-width="3038" src-height="1326" align="center"/>
    <img src="/assets/IAWabWTrVoE42TxeSmzjyGplpub.png" src-width="2990" src-height="1306" align="center"/>
    <img src="/assets/YOSdbRorQojWpQxcPHzjc2s5peT.png" src-width="2960" src-height="1282" align="center"/>
    <img src="/assets/I4LSb8sFsopai9xsW1HjpIWOpmb.png" src-width="2952" src-height="1394" align="center"/>
    - Select the target records and click the batch operation Pack for arrangement. If any records need to be removed from the batch before submission, this can be done within the pop-up window.
    - After submission for review,the batch moves to the Batch Pending page. The reviewer must perform work order approval; once approved, the withdrawal is completed.
    - Note: Due to withdrawal volumes and channel limitations, some withdrawal channels require manual status updates. In these cases, click View and update results and update the status manually in the pop-up window. (batch updates supported).
    - Once withdrawal is complete, the withdrawal file can be downloaded and saved locally.

<img src="/assets/Qvy3bvrwOoUZW5x8FVyjRl1Hpfb.png" src-width="2994" src-height="1270" align="center"/>

- Indicator Cards

For high-volume withdrawal scenarios, the system provides categorized indicator cards for refined operations. The cards are arranged from left to right in alignment with the sequence of business operations.

<img src="/assets/I00TbXlMJolXcVxmBEojpvjJpGe.png" src-width="2970" src-height="1334" align="center"/>

- Cheque Printing

If cheques are used as the withdrawal method and need to be printed after processing is complete, click Check Printing in the top-right corner of the page to enter the Check Printing page.

<img src="/assets/GXYzbrGgeoXK0ix93fpjUAwSpMf.png" src-width="2970" src-height="1304" align="center"/>

This page displays all withdrawal records processed via cheque. Select the target record, choose to perform an initial print or reprint (batch printing supported), enter the cheque number, and click OK to Print.

<img src="/assets/H2WrbgqrJolp4KxvKc8jayM3pUg.png" src-width="3020" src-height="1352" align="center"/>

## Withdrawal Reconciliation

To ensure the accuracy of fund flows and reduce the risk of financial loss, bank transactions must be reconciled against the system's withdrawal records. Bank statements can be sourced in two ways: (1) via API integration, which generates statements automatically, or (2) via manual import. For details, see the Withdrawal Bills section.

- Reconciliation: Users may refresh bank transactions for a selected period. The system will automatically match bank transactions with system withdrawal records. After reconciliation, review the Reconciliation Results column in the list — any discrepancies must be investigated.

<img src="/assets/L4nIbSA95oEG1rxehRljPJnVpub.png" src-width="2976" src-height="1332" align="center"/>

<img src="/assets/UWOmbS2HGoOqlrxD38XjCoiqprg.png" src-width="2938" src-height="1324" align="center"/>

## Withdrawal Exceptions

Operators can handle exceptions occurred during withdrawals or reconciliation in the Exception Processing pop-up window. (batch operations supported). The system provides four resolution methods:

- Set as Successful
- Set as Failed
- Repayment (regenerate the withdrawal order and attempt payment again)
- Resubmit (resubmit the original withdrawal order to the channel for payment)

<img src="/assets/QSwabuiXOo7kcKxEwPkjgS0yppA.png" src-width="2962" src-height="1322" align="center"/>

Once a resolution method is selected, the record moves to the To be reviewed category, where the operator should verify the outcome. The withdrawal exception is considered resolved upon approval.

<img src="/assets/PuLub4pgioYRkExmiP1jYxMgp3f.png" src-width="2984" src-height="1336" align="center"/>

## Withdrawal Records

The Withdrawal Records tab provides a complete log of the full lifecycle status of all withdrawals. Operators can query, export, and perform other operations on these records

<img src="/assets/S7t3bvtRIoWLsfxMv4OjzhFIpDW.png" src-width="2936" src-height="1312" align="center"/>

## Withdrawal Bills

Withdrawal bills comprise all debit transaction records associated with the broker's bank accounts and serves as an important basis for verifying withdrawal operations.

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Cash Management &gt; Bank Statement &gt; Withdrawal</p>
</div>

- If the bank supports direct bank-enterprise connection, the system can automatically obtain bank statements.
    - If direct connection is not available, back office operators must import statements manually using the bank's statement template.

<img src="/assets/S9WobCPWaoyAA4xzs0IjRTdfpWc.png" src-width="2988" src-height="1300" align="center"/>

<img src="/assets/MWAZblqnqoQpWWx0WDDjBt4ip0f.png" src-width="2990" src-height="1336" align="center"/>

- For bank statements obtained automatically or imported manually, iany entry confirmed to be a duplicate and with a match status of Unmatch may be deleted manually.

<img src="/assets/XeKBbEofwoSqDBx6huNjTljsptg.png" src-width="2970" src-height="1310" align="center"/>

- When bank statements are parsed, negative amounts may appear for bank debits, which could cause the system to incorrectly classify them as debits. If such cases are identified, they can be manually reclassified as credits.

<img src="/assets/RrW9bS7t9op1TExDLSsjfvDrprg.png" src-width="2968" src-height="1304" align="center"/>

- Withdrawal orders with an Unmatch status require manual association and tagging according to the actual debits.
    - If a tag was incorrectly applied, the operator can click Reject to reverse it.

<img src="/assets/TIpIbAvJ7o95NSxwRp0jcUeLpOb.png" src-width="2982" src-height="1396" align="center"/>

<img src="/assets/NocMbEknpoO0DAxemnJjH4M6p9Q.png" src-width="3048" src-height="1202" align="center"/>

