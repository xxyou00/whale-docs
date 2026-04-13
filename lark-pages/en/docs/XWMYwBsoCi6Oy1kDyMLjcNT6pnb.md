---
title: Deposit
slug: MrUFwI3r1iG4FrkDdSHcEgzrnSe
sidebar_position: 0
---


# Deposit

# 1. System Overview

Deposit refers to the process by which an investor transfers funds into their securities account. This process involves multiple steps to ensure that funds are securely and accurately credited to the investor’s account.

The Whale system includes functions for handling deposit applications, matching bank statement, deposit review, separate processing of deposits during account opening, reconciliation, and deposit record queries. To satisfy compliance and risk-control requirements, the system's design features multi-role, workflow-driven capabilities that balance high deposit efficiency with low financial risk.

As different brokerage firms have varying requirements for deposits—some require fast deposits, while others require precise matching of bank statements before deposit—the system supports two deposit workflows, as shown below:

<img src="/assets/ByiswEVTjhpYAabuAI2j1WaRpEd-board.jpeg"/>

# Prerequisites

None

# 2. Operation Instructions

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Cash Management &gt; Deposit</p>
</div>

## Deposit Application

A deposit application is initiated by the client. The application usually includes four main parts: currency, application amount, recipient bank card, and remarks. Whale operators can manually assist clients with deposit submissions and may reject an application or submit it for approval based on the the information provided by clients.

- Create (Deposit Application)

This function can be used when a client contacts a back-office operator to perform a manual deposit. The operator needs to select the client, deposit currency, deposit method, and beneficiary bank, enter deposit amount and remarks, and upload supporting documents (if any).

<img src="/assets/PkDobdc5YochnLxp1LFj3jJTpAc.gif" src-width="2086" src-height="994" align="center"/>

- Reject: If the deposit application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Reject.
- Delete: If the deposit application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Delete to remove the target record.
- Edit: If an issue is found with a client's deposit application before submission for approval, the operator can click Audit to correct it after confirming with the client. Edits require a work-order approval; changes take effect only after approval.
    - Editable fields: Deposit Currency, Deposit Method, Beneficiary Bank, Deposit Amount, Deposit Fee, Remarks, and Supporting Document
        <img src="/assets/D9Lvb6QTOoUjM4xW5mbjjiI1p8e.gif" src-width="2086" src-height="994" align="center"/>

- Submit (batch submission supported): Once the operator has completed a preliminary review and confirmed that all information is accurate, the application can be submitted to the next-stage operator for review and processing.
- Direct Deposit: For brokerages with time-sensitive deposit requirements, the Direct Deposit function streamlines the funding process. Upon receiving a client's deposit application, the operator only needs to supplement the bank statement details to complete the deposit. By default, Direct Deposit requires approval. To disable the approval requirement, contact the operations and maintenance team to adjust the configuration.
- Approval required: On the Credit directly page, verify that all information is correct, and then click Submit approval. The application will be routed to the deposit review page and processed upon approval.
- No approval required: On the Credit directly page, verify that all information is correct, and then click Deposit directly to complete the transaction immediately.

Approval required

<img src="/assets/CDEfb47FBoqUJ8xuqrWjen3QpOh.png" src-width="1700" src-height="1436" align="center"/>

No approval required

<img src="/assets/Fyg1bAhnXojjoWxEzaZjcSvPpCe.png" src-width="1698" src-height="1352" align="center"/>

## Deposit Match

The data on this page are derived from bank deposit statements. If a brokerage's business rules require bank statement entries to be matched with deposit records before funding, this can be handled manually on the Deposit Match page after confirming the bank statement information is synchronized with the system. The handling methods include linking for deposit and refund to clients.

<table header_row="1">
<colgroup>
<col width="224"/>
<col width="528"/>
</colgroup>
<thead>
<tr><th><p>Processing Method</p></th><th><p>Definition</p></th></tr>
</thead>
<tbody>
<tr><td><p>Linking</p></td><td><p>Automatically matching bank statement fields, such as the remitter&#39;s name, bank account number, currency, and amount, with existing deposit records for funding.</p></td></tr>
<tr><td><p>Deposit Refund</p></td><td><p>This method is used when an deposit cannot be accepted due to uncompleted account opening, account flagged for risks, or other reasons, and funds need to be returned to the client&#39;s account.</p></td></tr>
<tr><td><p>Withdrawal Refund</p></td><td><p>This method is used when a client&#39;s withdrawal is rejected by the beneficiary bank, and the funds are returned by the bank to the account, recorded as a bank inflow. This function allow the returned funds to be matched with the original account. (Since these returned funds appear as an inflow on the bank statement, they are managed on the Deposit Match page to ensure they are distinguished from regular deposits.)</p></td></tr>
</tbody>
</table>

- Link Checking: This page displays only those bank statement deposit entries that the system could not match automatically and therefore require manual review. Operators can follow the on-screen prompts to review each entry and proceed with subsequent deposit or other actions.
    - The Link Checking page will automatically compare fields based on name matching (as shown in the figure). If the result is correct, click Link.
    <div class="flex gap-3 columns-2" column-size="2">
    <div class="w-[41%]" width-ratio="41">
        <img src="/assets/RiI5bDRr0oNCfMxxX0Lj9wDdpCh.png" src-width="2484" src-height="1946" align="center"/>
        </div>
    <div class="w-[58%]" width-ratio="58">
        <img src="/assets/J0WKbaHClovxVfxSuIWjy9i5pHf.png" src-width="2574" src-height="1434" align="center"/>
        </div>
    </div>
    - If the system's suggested match is incorrect, click Customize to manually link the entry to the correct client. Manual linking can be performed using either a deposit application or a securities account.
    <div class="flex gap-3 columns-2" column-size="2">
    <div class="w-[50%]" width-ratio="50">
        <img src="/assets/IJtwbU0OFoVjOKxhwgVj0kUwpoh.png" src-width="3100" src-height="1756" align="center"/>
        </div>
    <div class="w-[49%]" width-ratio="49">
        <img src="/assets/LM9kbp5V5ostwaxcy2TjH0top1b.png" src-width="3030" src-height="1732" align="center"/>
        </div>
    </div>

Deposit Refund: This function is used when a deposit fails to reach the client's securities account for any reason and a refund must be issued. The operator should enter the client's bank account details, confirm the details, and click OK. The record will then be routed to the deposit review page for approval.

<img src="/assets/R07abr1wno5d46xCGzfjz0BfpKD.png" src-width="3392" src-height="1871" align="center"/>

Withdrawal Refund: The data on the Deposit Match page comes from inflows on bank statements, and a client withdrawal that has been rejected by the bank will appear as an inflow in the statement. The operator needs to link the withdrawal ID and process the entry using the Withdrawal Refund function.

<img src="/assets/LKVvbBFfEoMWbhxrUyDjUXpFpPg.png" src-width="3298" src-height="1760" align="center"/>

## Deposit Review

After operators process inflows on bank statements on the Deposit Match page, the results are sent to downstream reviewers for approval. Funds are only deposited after approval. For normally linked deposits, there are cases where the client's securities account is still in the opening process at the time of deposit. The system will separately approve such records.

- Opening: Select the target record, click Approve to enter the details page, recheck the information, and initiate a work order approval after confirmation.

<img src="/assets/NLDsbfvbWouBZ8xuzTRjfS5Hpge.png" src-width="3310" src-height="1748" align="center"/>

- Opened: Select the target record, click Approve to enter the details page, recheck the information, and approve directly after confirmation.

<img src="/assets/Amkkb1mWYo9ca9xxt0Dj1mvepLg.png" src-width="3310" src-height="1748" align="center"/>

- Deposit refund: Select the target record and click Approve to trigger the approval work order. Confirm the details and approve.

<img src="/assets/P5LYbmCKQo0HHyxMvIujnZ4BpHb.png" src-width="3320" src-height="1762" align="center"/>

- Withdrawal refund: Select the target record, click Approve, and approve directly upon confirmation. No work order approval is required.

<img src="/assets/Km9YbtdHZonXdXxGOsmjTLLVpWq.png" src-width="3401" src-height="1852" align="center"/>

## Deposits During Account Opening

Since the deposit and account opening workflows can be initiated in parallel, there are cases in which the deposit workflow has been approved while the account opening workflow is still in progress. This page allows operators to monitor the account opening status corresponding to each approved deposit record.

Operators can view the status of each record in the Account Opening Status column. If a client's account opening fails, click Reject to reject the associated deposit record (batch operations supported).

<img src="/assets/Rw3OblWgzoktvixY9Lcj25j8pxe.png" src-width="3288" src-height="1122" align="center"/>

## Deposit Reconciliation

To ensure the accuracy of fund flows, business operations require comparing bank statement entries with system deposit records to improve deposit accuracy. There are two sources of bank statements: (1) API integration (automatic), and (2) manual import.

- Reconciliation: Operators can select the bank statement for the target period to refresh. The system will automatically match the bank statement entries with the system's deposit records. After reconciliation is complete, operators can check the results in the Reconciliation Results column. If inconsistencies are found, further investigation and handling are required.

<img src="/assets/ATF2bW9nAoFdLIxo5ecjNMcDp7f.png" src-width="3282" src-height="1496" align="center"/>

<img src="/assets/LacLb6unJoORwNxl1A8je1Mzp2d.png" src-width="3290" src-height="1732" align="center"/>

## Deposit Records

The Deposit Records page tracks the full process of deposits. Operators can query, export, and import records on this page at any time.

- If operators did not enter bank statement information when using the Direct Deposit function, they can click Import bank statements to supplement bank statement information in batches on this page.

<img src="/assets/LHlvbv9IyoosAqxgknCjoAISp9g.png" src-width="3784" src-height="1458" align="center"/>

# 3. FAQ

Q: What are the deposit methods and channels?

A: Common deposit methods include: online banking transfer, wire transfer, bank-securities transfer, sub-account transfer, eDDA, Faster Payment System (FPS), cheque, ATM/bank counter, and PayNow.

Q:

A:

Q:

A:

Q:

A:

