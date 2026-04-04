---
title: System Introduction
slug: HiW6wXbmYiYpnPkuZ3yckwxQnXf
sidebar_position: 2
---


# System Overview

## 1. System Overview

Deposit refers to the process by which an investor transfers funds into their securities account. This process involves multiple steps to ensure that funds are securely and accurately credited to the investor’s account.

The Whale system includes functions for handling deposit applications, matching bank statement records, deposit review, separate processing of deposits during account opening, reconciliation, and deposit record queries. To satisfy compliance and risk-control requirements, the system's design features multi-role, workflow-driven capabilities that balance high deposit efficiency with low financial risk.

As different brokerage firms have varying requirements for deposits—some require fast deposits, while others require precise matching of bank statements before deposit—the system supports two deposit workflows, as shown below:

<img src="" src-width="100" src-height="100" align="center"/>

# Prerequisites

Operators must obtain the following permissions before they can use the system functions.

<table header_row="1">
<colgroup>
<col width="289"/>
<col width="490"/>
</colgroup>
<thead>
<tr><th><p>Permission Name</p></th><th><p>Permission Description</p></th></tr>
</thead>
<tbody>
<tr><td><p>Permission to manage funding parameters, bank statements, and deposits</p></td><td><p>Permission to manage bank statements, deposit and withdrawal records/methods, bank cards, foreign-exchange services, and funding guidelines; and fund parameter configuration</p></td></tr>
</tbody>
</table>

## 2. Operation Instructions

# Deposit Configuration

# Funding Parameter Configuration

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Business Parameters Settings &gt; Fund Parameter</p>
</div>

1. Company Bank Accounts

Before a client can deposit funds, the corresponding company bank account needs to be added in the back office, and the deposit methods supported under that company bank account need to be configured.

<img src="/assets/AaI6bjXdyoq8L2xXQIpj1D34pSb.png" src-width="3294" src-height="996" align="center"/>

Operation button descriptions:

- Add: Add company bank account information for the brokerage as needed.
- Edit: Manually edit existing company bank account information.

1. Currency

Deposit currencies must be configured in the system before clients can initiate deposits.

<img src="/assets/PVutbQfxaoeptexpJIbjxmXHpng.png" src-width="3288" src-height="852" align="center"/>

Operation button descriptions:

- Add: Add currencies as required by the brokerage.
- Edit: Manually edit existing currency entries.

# Client Bank Card

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; Bank Card Management</p>
</div>

Clients must configure their bank card information with the broker. Bank cards can be added either by the clients via the client app or by back office operators.

<img src="/assets/LSCpbwDfao104bxsaWPju2tCpjh.png" src-width="3314" src-height="970" align="center"/>

Operation button descriptions:

- Batch Add: Add bank card information in batches according to a template.
- Add bank cards: Add a single bank card.
- Recycle Bin: Display deleted bank card records.
- Set Rejection Reason: Configure reasons for rejecting a bank card.
- Review: Review the bank card in the back office.
- Remark: View remarks related to the bank card.
- Delete: Delete bank card information.
- Update Deposit Witness Status: Associate with the client's deposit details and update the bank card's deposit witness status from Pending Witness to Witnessed. 

# eDDA Authorization

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p> Cash Management &gt; Bank Card Management</p>
</div>

If a customer intends to deposit via eDDA, eDDA authorization is required. After a client completes eDDA authorization, the corresponding record can be viewed in the back office.

<img src="/assets/V9WjbBK2zolss0xQHeWjdIFypce.png" src-width="3290" src-height="1004" align="center"/>

Operation button descriptions:

- Refresh icon: Retrieve the latest eDDA authorization records.
- Remark: Configure remarks for the authorization record.
- Modify Status: Modify the status of an authorization record.
- Delete: Manually delete authorization records that are in-progress.

# Bank-Related Information Configuration

The enumeration values used when setting up client or company bank account information—including common banks, countries/regions, and bank regions—can all be configured through the back office.

## 1. Card-Issuing Bank

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; App Config &gt; Supported Bank Setups</p>
</div>

<img src="/assets/UiExbvngho8Ln3xvnrWj3qLspOh.png" src-width="3292" src-height="712" align="center"/>

Operation button descriptions:

- Add: Add a single entry to the list of common banks for each region.
- Edit: Edit existing entries in the bank list.

## 2. Client Card Binding - Country/Region

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; App Config &gt; Bank Card Country/Region</p>
</div>

<img src="/assets/AHt8bdkHBoyb0Ax7voijxhg9pnc.png" src-width="3286" src-height="786" align="center"/>

## 3. Bank Region List

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; App Config &gt; Bank Region List</p>
</div>

<img src="/assets/WojAbPZuBoZTYIxqrD3jAHwApYd.png" src-width="3288" src-height="992" align="center"/>

Operation button descriptions:

- Add: Add a single entry to the bank region list
- Edit: Edit existing entries in the bank region list
- Delete: Delete an entry from the bank region list

# Deposit Guidance Configuration

The operation guidelines and deposit parameters for the client deposit page can be configured in the back office.

## 1. Deposit Guidelines

<img src="/assets/JhRfbPQhToJzGtxLQMmjhai8p2g.png" src-width="3276" src-height="840" align="center"/>

## 2. Deposit Parameters

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; App Config &gt; Deposit Parameter Setups</p>
</div>

<img src="/assets/Kyvub3dc4ofyE3x6CkJjrucBp2d.png" src-width="3274" src-height="984" align="center"/>

Operation button descriptions:

- Add: Add a single deposit parameter entry.
- Edit: Edit existing deposit parameter entries.
- Delete: Delete a deposit parameter entry from the list
- Publish: Display the configured deposit parameter on the client app.
- UnShelve: Hide the configured deposit parameter from the client app.
- Copy: Quickly Add a new deposit parameter by copying the information from an existing one.
- Approval: If a work order approval is enabled for deposit parameters, all the above operations require work order approval after submission.

Multiple Receiving Bank Configuration

- If the client app needs to display multiple receiving banks under the same deposit method based on the bank selected by the client, the configuration shown in the following screenshot can be referred to.

<img src="/assets/TpPNbsmTkoprMZxiqAujYXSMpqd.png" src-width="3274" src-height="984" align="center"/>

# Deposit Operations

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Cash Management &gt; Deposits</p>
</div>

# Deposit Applications

A deposit application is initiated by the client. The application usually includes four main parts: currency, application amount, recipient bank card, and remarks. Whale operators can manually assist clients with securities funding and perform operations such as rejection and submission for approval.

- Add (Deposit Application)

This function can be used when a client contacts a back office operator to perform a manual deposit. The operator needs to select the client, deposit currency, deposit method, and beneficiary bank, enter deposit amount and remarks, and upload supporting documents (if any).

<img src="/assets/N5KAbcwL3oT5N5xL6kKjP4Vjpae.gif" src-width="2086" src-height="994" align="center"/>

- Reject: If the deposit application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Reject.
- Delete: If the deposit application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Delete to remove the target record.
- Edit: If an issue is found with a client's deposit application before submission for approval, the operator can click Audit to correct it after confirming with the client.
    - Editable fields: Deposit Currency, Deposit Method, Beneficiary Bank, Deposit Amount, Deposit Fee, Remarks, and Supporting Document 
    <img src="/assets/VtIVbnYLLoh4N0xmubHjsPEXp0d.gif" src-width="2086" src-height="994" align="center"/>

Operations

- Direct Deposit: For brokers with time-sensitive deposit requirements, the Direct Deposit function streamlines the funding process. Upon receiving a client's deposit application, the operator only needs to supplement the bank statement details to complete the deposit. By default, Direct Deposit requires approval. To disable the approval requirement, contact the operations and maintenance team to adjust the configuration.
    - Approval required: On the Credit directly page, verify that all information is correct, and then click Submit approval. The application will be routed to the deposit review page and processed upon approval.
    - No approval required: On the Credit directly page, verify that all information is correct, and then click Deposit directly to complete the transaction immediately.

Approval required

<img src="/assets/JC8ebJxEToomqixgQbRjYJs3prf.png" src-width="1280" src-height="1081" align="center"/>

No approval required

<img src="/assets/ZEedba1tsoHLT0xmXBDjWqGvpFg.png" src-width="1280" src-height="1019" align="center"/>

- Voucher Association: If the posting operation involves multiple applications, you may enter the Voucher Association page to perform batch postings.

<img src="/assets/BeaGbkXJeo0pTnxjqOJjQn2Dpye.png" src-width="1267" src-height="411"/>

On the Vouchers associated page, all applications pending deposit will be displayed automatically. The operator can review, select, and submit applications for funding.

<img src="/assets/P1NVbUDaMoG6Q5xDI77jeRhepHf.png" src-width="1280" src-height="415" align="center"/>

On the Voucher Association page, all applications awaiting posting are filtered and presented for operator selection; after verification, submit to post.

<img src="/assets/S0nAbI8gqow5qrxIkTxjMQxEpqh.png" src-width="1280" src-height="603" align="center"/>

# Deposit Match

The data on this page are derived from bank deposit statements. If a brokerage's business rules require bank statement entries to be matched with deposit records before funding, this can be handled manually on the Deposit Match page after confirming the bank statement information is synchronized with the system. The handling methods include linking for deposit and refund to clients.

<table header_row="1">
<colgroup>
<col width="160"/>
<col width="499"/>
</colgroup>
<thead>
<tr><th><p>Processing Method</p></th><th><p>Definition</p></th></tr>
</thead>
<tbody>
<tr><td><p>Linking</p></td><td><p>This method is used to automatically match bank statement fields, such as the remitter&#39;s name, bank account number, currency, and amount, with existing deposit records for funding.</p></td></tr>
<tr><td><p>Deposit Refund</p></td><td><p>This method is used when an deposit cannot be accepted due to uncompleted account opening, account flagged for risks, or other reasons, and funds need to be returned to the client&#39;s account.</p></td></tr>
<tr><td><p>Withdrawal Refund</p></td><td><p>This method is used when a client&#39;s withdrawal is rejected by the beneficiary bank, and the funds are returned by the bank to the account, recorded as a bank inflow. This function allow the returned funds to be matched with the original account. (Since these returned funds appear as an inflow on the bank statement, they are managed on the Deposit Match page to ensure they are distinguished from regular deposits.)</p></td></tr>
</tbody>
</table>

- Link Checking: This page displays only those bank statement deposit entries that the system could not match automatically and therefore require manual review. Operators can follow the on-screen prompts to review each entry and proceed with subsequent deposit or other actions.
    - The Link Checking page will automatically compare fields based on name matching (as shown in the figure). If the result is correct, click Link.
    <img src="/assets/ZI2ibnTF3o4sCNx0Nu4jqar0pdh.png" src-width="3276" src-height="1742" align="center"/>
    <img src="/assets/Oj2FbrxlPoBJlJxkP47jz55upac.png" src-width="3390" src-height="1838" align="center"/>
    <img src="/assets/HKYKbn2LRoEY22xkKA9jQUhQpOc.png" src-width="3286" src-height="1758" align="center"/>
    <img src="/assets/W3Lbb1cRLoPwdvxB3T3jvOp0pff.png" src-width="3260" src-height="1748" align="center"/>

- Deposit Refund: This function is used when a deposit fails to reach the client's securities account for any reason and a refund must be issued. The operator should enter the client's bank account details, confirm the details, and click OK. The record will then be routed to the deposit review page for approval.

<img src="/assets/BKwybgQvIoVrEqxt0dfjW7LgpFc.png" src-width="3320" src-height="1768" align="center"/>

- Withdrawal Refund: The data on the Deposit Match page comes from inflows on bank statements, and a client withdrawal that has been rejected by the bank will appear as an inflow in the statement. The operator needs to link the withdrawal ID and process the entry using the Withdrawal Refund function.

<img src="/assets/HsS8bdAjuowxnkxQHI3jmvUhp2e.png" src-width="3292" src-height="1754" align="center"/>

# Deposit Review

After operators process inflows on bank statements on the Deposit Match page, the results are sent to downstream reviewers for approval. Funds are only deposited after approval. For normally linked deposits, there are cases where the client's securities account is still in the opening process at the time of deposit. The system will separately approve such records.

- Opening: Select the target record, click Approve to enter the details page, recheck the information, and initiate a work order approval after confirmation.

<img src="/assets/YnyZbhKLso3kWYxeC2UjtMJkpLe.png" src-width="3310" src-height="1754" align="center"/>

- Opened: Select the target record, click Approve to enter the details page, recheck the information, and approve directly after confirmation.

<img src="/assets/L2ulbcuk5olnFKxKtGdjTJatpU2.png" src-width="3310" src-height="1754" align="center"/>

- Deposit refund: Select the target record and click Approve to trigger the approval work order. Confirm the details and approve.

<img src="/assets/XAk7bcqrboxOL4xSLCoj9zsmpIg.png" src-width="3318" src-height="1748" align="center"/>

- Withdrawal refund: Select the target record, click Approve, and approve directly upon confirmation. No work order approval is required.

<img src="/assets/NyhubKx0Bo59nWxuQhKjSpQYpDb.png" src-width="3310" src-height="1768" align="center"/>

# Bank-Securities Transfer Deposit

After a bank-securities account is opened, clients can make deposits via bank-securities transfer. Upon receiving a bank notification, the system will automatically match the client and complete the deposit without requiring manual intervention.

<img src="/assets/ErWebCKKdoj3NcxECNmj894wpwh.png" src-width="3300" src-height="1226" align="center"/>

# eDDA Deposit

After eDDA authorization is completed, clients can make deposits via eDDA. Upon receiving a bank notification, the system will automatically match the client and complete the deposit without requiring manual intervention.

<img src="/assets/AUTcbqMkzouviax9dfOjPh1jp5a.png" src-width="3264" src-height="1230" align="center"/>

# Faster Payment System (FPS)

For FPS transfers, the system can automatically match the bank statement with the deposit application after receiving the statement. Once matched, the system can automatically complete the deposit.

<img src="/assets/IOpTb0EAfoG3FDxBXZZjdMqvpNf.png" src-width="3270" src-height="1256" align="center"/>

# Deposits During Account Opening

- If the client has selected transfer verification as the verification type, the deposit must be processed through a deposit application. For details, see "Application-Based Deposit".
- If the client has selected cheque verification and did not submit deposit application from the client app, the deposit must be processed based on the bank statement. For details, see "Bank Statement-Based Deposit".

Since the deposit and account opening workflows can be initiated in parallel, there are cases in which the deposit workflow has been approved while the account opening workflow is still in progress. This page allows operators to monitor the account opening status corresponding to each approved deposit record.

Operators can view the status of each record in the Account Opening Status column. If a client's account opening fails, operators can click Reject to reject the associated deposit record (batch operations supported).

<img src="/assets/L78RbLn4HoOJXTxalRpjP6J3phd.png" src-width="3288" src-height="966" align="center"/>

# Deposit Reconciliation

To ensure the accuracy of fund flows, business operations require comparing bank statement entries with system deposit records to improve deposit accuracy. There are two sources of bank statements:① API integration (automatically generated), and ② manual import.

- Reconciliation: Operators can select the bank statement for the target period to refresh. The system will automatically match the bank statement entries with the system's deposit records. After reconciliation is complete, operators can check the results in the Reconciliation Results column. If inconsistencies are found, further investigation and handling are required.

<img src="/assets/VvKBbD4wcokaqWxOVipj61XFpFd.png" src-width="3318" src-height="1486" align="center"/>

<img src="/assets/HMWrbUKoZoIOgQxP963jwV4Npnd.png" src-width="3286" src-height="1528" align="center"/>

# Deposit Records

The Deposit Records page tracks the full process of deposits. Operators can query, export, and import records on this page at any time.

- If operators did not enter bank statement information when using the Direct Deposit function, they can click Import bank statements to supplement bank statement information in batches on this page.

<img src="/assets/QrnJbnERbolNbVxu2rfjyiPCpxd.png" src-width="3808" src-height="1380" align="center"/>

- For cheque deposits that are already frozen, they can be manually unfrozen in the back office before the Estimate thawing time, or they can wait for the system to automatically unfreeze them.

<img src="/assets/UkZmb0Y6wov0r6xBe4kjyRn6pag.png" src-width="3268" src-height="1170" align="center"/>

- After manually submitting an unfreezing application, the operator needs to wait for work order approval.

<img src="/assets/NRutb1vvToEopxxLRoqjGd5CpdG.png" src-width="3284" src-height="1086" align="center"/>

