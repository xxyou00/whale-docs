---
title: Quick Start
slug: VSILwnfItiP6L8kcBWzcFptAnve
sidebar_position: 3
---


# Quick Start

# Overview

Whale's fund management system provides multi‑scenario withdrawal capabilities, allowing operators to submit clients' withdrawal requests, approve withdrawals, track exception records during the withdrawal process, and query all historical records.

# Quick Start

## Prerequisites

1. Configure company bank account withdrawal methods

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Fund Parameter &gt; Company Bank Account</p>
</div>

<img src="/assets/QHnebiNeAolvWNxXfd9jEHXUp9f.png" src-width="1280" src-height="574" align="center"/>

- Click Create to open the configuration page and add the relevant withdrawal channel information. A withdrawal channel is defined as the combination of the broker's payment bank account and withdrawal method, for example, ICBC Asia 001 — Cheque Transfer.

<img src="/assets/Zdt7bR3seotqGzx7PUPjeNSRp5c.png" src-width="1280" src-height="567" align="center"/>

1. Enable the withdrawal function for the currency

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Service Parameter &gt; Fund Parameter &gt; Currency Setup</p>
</div>

<img src="/assets/CbHobX9ZhoJ5oWxcJyCjCae7p8g.png" src-width="1280" src-height="574" align="center"/>

- Click Add to open the configuration page and select Yes for the Withdrawal Function option.

<img src="/assets/HCkeb3YIHoYQQMxJtO1jUCXyprc.png" src-width="1280" src-height="588" align="center"/>

## Processing Withdrawal Requests

Based on the client's withdrawal requirements, withdrawal requests can be manually created on the page. If a client has already submitted a withdrawal request via the app, the record will appear automatically on this page.

### Manual Withdrawal

Click Manual Withdrawal. In the pop-up window, select the client, currency, amount, and bank card, add any relevant remarks, and click Confirm Withdrawal to generate the request record (the system will automatically display the withdrawable balance for each currency based on the selected client).

<img src="/assets/N8F5bEXD2oMI8QxH4MvjEXwCpeh.png" src-width="1204" src-height="3012" align="center"/>

### Request Submission

After the request record is generated, the back-office risk control system will automatically validate its legitimacy, which takes about five seconds; once the risk control check passes, click Submit to proceed to the withdrawal steps.

<img src="/assets/Drlabh2vOonrJUxwRhJjElA0pUg.png" src-width="2988" src-height="1202" align="center"/>

## Withdrawal Processing

After a withdrawal request is submitted, the personnel responsible for executing the withdrawal will determine the appropriate handling method according to actual circumstances. The system provides two withdrawal modes: Direct Withdrawal and Batch Withdrawal. In addition, as withdrawal channels may be subject to daily limits, the system includes daily limit monitoring, management, and viewing functions to help reduce withdrawal exceptions.

### Direct Withdrawal

<b>Step 1:</b> Go to the Pending category under the Withdrawal - Pending tab, select the target record, verify that all information is correct, and click Direct billing.

<img src="/assets/Ld0hbXjmUosj6lxHSjOjfkpopXK.png" src-width="1280" src-height="573" align="center"/>

<b>Step 2:</b> In the pop-up window, enter the bank name, bank account, channel, and bank transaction reference (if applicable), and then click Submit for approval. If work order approval is not required, this step can be skipped. See Step 5 below.

<img src="/assets/Rkinbg4hpo7Rf8xAqgYj0nRwptc.png" src-width="1280" src-height="573" align="center"/>

<b>Step 3:</b> Go to the work order system, locate the record submitted for review, and complete the audit.

<img src="/assets/HfYFbZS3yoUdB1xpmNGjCRTXpHQ.png" src-width="1280" src-height="540" align="center"/>

<img src="/assets/EtwabIEYHoocloxcOgVjE81sp7f.png" src-width="1280" src-height="581" align="center"/>

<b>Step 4:</b> In the Deposit Directly Pending category, select the target record, and click View and update result to manually update the withdrawal status. Setting the status to Success completes the withdrawal.

<img src="/assets/FpF2bRPLqoLTGHx3oLhjRYO2pvh.png" src-width="3320" src-height="1020" align="center"/>

<img src="/assets/W1JQbcBIeo0tQDxUUD9jMPmepsf.png" src-width="3316" src-height="1728" align="center"/>

<img src="/assets/WgP5b4fjZoVkq6xWjnfjC0kEpib.png" src-width="3324" src-height="592" align="center"/>

<b>Step 5:</b> If work order approval is not required, go to Service Parameter &gt; Withdrawal Rules Management &gt; More settings to turn off the approval switch.

<img src="/assets/Q4B7bgcnDoMGisxHQgPjvVZmpdg.png" src-width="3816" src-height="1780" align="center"/>

### Batch Withdrawal

<b>Step 1:</b> In the Pending category, select multiple target records and click Pack for Arrangement.

<b>Step 2:</b> In the popup, fill in the relevant bank information and click Submit for approval.

<img src="/assets/NdxybRFvtoKKXFxRfuyjy5Urpys.png" src-width="1280" src-height="558" align="center"/>

<b>Step 3:</b> Go to the Batch Pending category, select the batch just created, click Audit, and complete the approval in the triggered work order.

<img src="/assets/TKGSbsTbmoZhyZxDLJOjRWZsp9p.png" src-width="1280" src-height="559" align="center"/>

<b>Step 4:</b> Click Direct updates on the batch record to open the pop-up window, and then update the status of each record within the batch to Success based on actual withdrawal results (batch operations are supported).

<img src="/assets/ZEoubkV7Uo67Hex360KjWXlcpLh.png" src-width="1280" src-height="599" align="center"/>

<b>Step 5:</b> Go to the work order system to re-audit the updated results. Once approved, the withdrawal is complete.

<img src="/assets/DDF5b92emoVqUSxNhmQj7dvHpXb.png" src-width="1280" src-height="554" align="center"/>

<img src="/assets/FVNGbKvydoHwzzx5EPajFMYapRb.png" src-width="3746" src-height="1758" align="center"/>

### Daily Limit Configuration

As withdrawal channels may be subject to daily limits, daily limit monitoring and management functions are available to help minimize withdrawal exceptions.

<b>Step 1:</b> Go to Service Parameter &gt; Withdrawal Rules Management &gt; Daily limits. The page displays all currently configured limits.

<img src="/assets/WFH6b8weuoUi0OxxNtxjyA6npni.png" src-width="1280" src-height="325" align="center"/>

<b>Step 2:</b> To add a new limit, click Add, complete the required fields in the pop-up window, and click OK.

<img src="/assets/DCJMbJm5OoDJC0xrfpzjQyRSp0g.png" src-width="3802" src-height="1800" align="center"/>

- To adjust an existing limit, click Adjust in the Action column, select Manual increase or Manual reduce in the pop-up window, and enter the adjustment amount.

<img src="/assets/Ov3QbntAfoNambxRZVxje3C6pXg.png" src-width="3006" src-height="1352" align="center"/>

- To modify other fields, click Edit in the Action column to open the pop-up window and make changes.

<img src="/assets/IvB3bWtHOoMb5Tx2w1JjjtsjpMT.png" src-width="3006" src-height="1312" align="center"/>

- To delete a record, select the record and click Delete in the Action column.

<img src="/assets/INBPbw1KmoiXdgxyEN5jJaMepOb.png" src-width="2994" src-height="868" align="center"/>

- To view limit change history, navigate to Service Parameter &gt; Withdrawal Rules Management &gt; Daily Limit Changes

<img src="/assets/SmghbT2drog5kgxREPNjV0Lnpqe.png" src-width="1280" src-height="575" align="center"/>

## Handling Withdrawal Exceptions

In practice, withdrawals may be rejected by banks for various reasons; such records will be marked as exceptions and require manual handling.

<b>Step 1:</b> In the Pending category, select the target record and click Handle. In the pop-up window, select one of the four available handling options and click OK.

<img src="/assets/JhSDbB6Oto4d7BxjAP1jq3pNpyb.png" src-width="3000" src-height="1354" align="center"/>

<b>Step 2:</b> Go to the To be reviewed category, select the target record, and perform a recheck.

<img src="/assets/FGIIbdqBEojHDsxtYzKjy58npxh.png" src-width="2996" src-height="1310" align="center"/>

