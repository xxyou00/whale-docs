---
title: System Overview
slug: 2a05bab0c2cc81d3a79adcc4e47cf1e0
sidebar_position: 2
---


# System Overview

# I. System Overview

This guide outlines the comprehensive back office operational workflow for cryptocurrency deposit services, encompassing record generation, query and tracking, exception handling, cancellation, and the refund process. It is intended to ensure standardized operations by back office operators and to maintain business compliance and fund security.

# Prerequisites

- The back office operator has logged in to WBO using dedicated credentials and navigated to VA Clearing Management &gt; Deposit & Withdrawal &gt; Deposit.
- The account holds the necessary permissions for operations such as deposit application, deposit records, cancellation, and refund. Operators who have not been granted the required permissions should contact the administrator to request access.

# II. Operation Instructions

## Cryptocurrency Configuration

Operators should configure cryptocurrency settings for deposits before processing client deposits.

<img src="/assets/Qs63bldUWoUhdqxC9LpjVuKFpsd.png" src-width="1280" src-height="614" align="center"/>

## Client Wallet Address

To ensure asset security, wallet address verification must be completed before a deposit is processed. This is a critical prerequisite step.

<img src="/assets/Hgj7bqIK6oFrMVxqUYJj85BCpgd.png" src-width="1280" src-height="610" align="center"/>

## Deposit Operations

<b>Request Reception and Record Generation</b>

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Deposit Application</p>
</div>

- After the client submits a deposit request, the system automatically receives the request information and generates a unique deposit record (including record number, client securities account, deposit currency, amount, destination address, transaction hash (TXID), request time, status, and other core information).
- For deposit applications with exceptions or errors, back office operators can delete them directly in the system.

<img src="/assets/LUNXbD0T4om70DxLiR9jAo4rplW.png" src-width="1280" src-height="336" align="center"/>

<b>Deposit Record Query and Tracking</b>

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Coin Deposit Records</p>
</div>

- <b>Multi-condition Query: </b>Records can be filtered by criteria such as record ID, client ID, creation time, and status, allowing operators to quickly locate the target record.
- <b>Progress Tracking: </b>The full deposit process can be monitored in real time. Operators can click a record to view its details, including address verification status and blockchain confirmation progress associated with the transaction hash.

<img src="/assets/PAYtbvktAoeU9Tx9QudjsDgSpef.png" src-width="2446" src-height="964" align="center"/>

<b>Cancellation of Unprocessed Deposit Records</b>

- <b>Prerequisite</b>: This operation applies only to records in the Wallet Auth Pending status (i.e., deposit requests for which blockchain network confirmation has not started and assets have not been transferred out). Records in other statuses cannot be canceled.
- <b>Operation steps:</b>:
    1. In the deposit records list, locate the target record and click Cancel.
    2. In the confirmation pop-up window, enter an operation note (e.g., "Duplicate application" or "Incorrect address provided") and confirm the cancellation.;
    3. Upon successful cancellation, the record status will be updated to Canceled. The system automatically retains a cancellation operation log (including operator, operation time, and note) for future tracing.

<img src="/assets/MMKDbz6nQoboX4xMiwCjWYoJpjb.png" src-width="2480" src-height="696" align="center"/>

<b>Refund After Successful Deposit</b>

- <b>Prerequisite</b>: This operation applies only to records in the Success status (i.e., assets have been successfully credited to the platform, and the client applies for a refund or the system requires a forced refund). Operators shall verify the client's identity and the reason for the refund..
- <b>Operation steps:</b>:
    1. Enter the Deposit page, find the target deposit record, and click Withdraw coins.
    2. Fill in Refund Information: Enter the client-specified refund address (must match the client's identity verification information), select the corresponding network (must match the deposit network), and verify the refund amount (defaults to the deposit amount; can be adjusted with a reason noted for the adjustment).
    3. Execute Refund Operation: Click Execute Refund. The system generates a refund transaction hash and synchronizes it to the blockchain network.
    4. Track Refund Status: Monitor the blockchain confirmation progress of the refund record in real-time. Upon completion, update the deposit record status to refund and keep the full-process log of the refund.
    5. Notify Client: Upon successful refund, notify the client through offline channels.

<img src="/assets/BJjcbxXoRocUVRxxSqjjdw2upig.png" src-width="2452" src-height="732" align="center"/>

