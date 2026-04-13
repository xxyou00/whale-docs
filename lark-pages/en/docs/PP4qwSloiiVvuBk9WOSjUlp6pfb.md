---
title: System Introduction
slug: T0JSwBdbmiU6aNkKRp0cW5q0nSf
sidebar_position: 2
---


# System Overview

# System Introduction

## I. System Overview

The securities transfer-in feature enables investors to transfer securities holdings into their securities accounts through the securities trading platform. This feature allows investors to efficiently transfer securities, enabling them to participate in securities trading and investment activities anytime, anywhere.

The Whale system includes functions such as transfer-in application, transfer-in details, streamlined import parameter settings, and email notification to brokers. The process supports the review requirements of different roles and effectively improves the accuracy of securities transfer-in. The overall process is as follows:

<img src="/assets/QeAbwYwJqhgu5gbphrFjIHg2p7e-board.jpeg"/>

## II. Operation Instructions

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Stock Management &gt; Transfer In</p>
</div>

### Transfer-In Application

A transfer-in application is initiated by the client and consists of four components: broker information, account information, securities details, and remarks. Back office operators can create applications manually on a client's behalf, and may take the following actions on any submitted application: reject, submit for approval, or notify the delivering broker.

- Manual Transfer-in

This applies when a client contacts a back office operator to request a manual transfer-in. The operator must enter the client's security details and account information.

<img src="/assets/OLmjbiLzroUchex3D9Djx3jTpSh.png" src-width="1280" src-height="570" align="center"/>

- If the shares to be transferred in are physical stock, select Yes for Whether it is a physical stock..
- Reject (batch operation supported): If the transfer-in application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Reject.
- Notify Broker: Since transfer-in operations require cooperation from the delivering broker, in practice, operators need to contact the delivering broker to ensure a timely transfer-in. The Notify Broker function provides an in-system email tool that allows operators to send notifications to the delivering broker. Email delivery results are displayed to operators, giving them visibility into whether the broker has been notified.
    - Select the broker institution to which the email should be sent. The system will automatically populate the broker's email address. The operator should verify that the email address is correct.
    - Select the securities transfer-in application details under the target broker. (Already-sent application details will be excluded.)
    - Preview the email content, and click OK after confirming it is correct.
    - Go to the Email Records tab to check the sending status.
    <img src="/assets/StcGbnisloXhnqxNXbcjBmx6p9k.png" src-width="1280" src-height="572" align="center"/>
    <img src="/assets/VIImb0HRMoP4xdxghzWjfcZEpRb.png" src-width="1280" src-height="567" align="center"/>
    <img src="/assets/X31jbm0siofGfPxyF8ijugQgpOc.png" src-width="3022" src-height="1310" align="center"/>
    <img src="/assets/LfNybNyQIoqNpuxamrqjVvYrpLh.png" src-width="2964" src-height="1322" align="center"/>

- Submit (bulk operation available): After the operator's preliminary review confirms correctness, the application may be submitted to the next-node operator for review — the deposit entry operation.
- Edit: If, during processing the transfer application, the operator learns from the client whether the broker has been notified or not, the operator can use the [Edit] button to modify the notification status so that the broker's awareness matches the actual situation.

<img src="/assets/SHfDbwsAnopDDex3i22jLrk4pvd.png" src-width="2954" src-height="1346" align="center"/>

- Metric Cards

If a broker's securities transfer-in volume is high, the system's categorized display cards can be used for more granular operations. The left-to-right arrangement of the metric cards reflects the sequence of business operations.

<img src="/assets/KNJObwgmpoO5RyxHbQ2jvIHppFT.png" src-width="2988" src-height="1330" align="center"/>

### Deposit Details

Because a single deposit application may contain multiple security detail records, the deposit processing reviewer must carefully verify each deposit detail; only after approval may the deposit be entered.

- Edit: If, during processing of security details, a specific detail record submitted by the user is found to be erroneous, it may be corrected via the [Edit] button after confirmation with the client.
    <img src="/assets/VC4rb7uD0ofUnOx7vqNjo7Mspyf.png" src-width="3002" src-height="1244" align="center"/>
    - Editable fields: stock name, custodian code, sub-account number, security detail quantity, transfer cost, and settlement remarks.

- Delete: If the user indicates that a specific submitted detail will no longer be transferred, the target detail record can be removed via the [Delete] button.
- Generate SI Instructions (bulk operation available): Because transfer-in operations require necessary SI information to be entered in CCASS, the "Generate SI Instructions" function can automatically save this required information as a file for users to upload to CCASS, avoiding manual entry in the CCASS system. Generated SI instructions can also be viewed and exported under the "SI Instruction List" menu.

<img src="/assets/Fb75boLeeoJGiNxEDSijWuvDpUg.png" src-width="2992" src-height="1236" align="center"/>

<img src="/assets/GWvjba7LIouY6oxpKQZjKddnpvg.png" src-width="2970" src-height="1304" align="center"/>

- Edit SI Instructions (bulk operation available): If modifications are required to generated SI information, select [Edit SI Info] to correct the target fields.

<img src="/assets/Y4NobzIZ8oPYy5xhCs0jcfTOphh.png" src-width="2990" src-height="1306" align="center"/>

- Process — Successful Submission / Failed Submission (bulk operation available): If the operator determines that a detail has no issues, they may select [Process] and choose "Successful Submission"; otherwise, choose "Failed Submission".
    <img src="/assets/Ub60bzRAboB4fTxy8nXjkAvWpuc.png" src-width="1280" src-height="446" align="center"/>
    <img src="/assets/Er8vbezLzoWIOpxUzncjdAZgpVe.png" src-width="1280" src-height="641" align="center"/>
    - After processing, the workflow proceeds to the next node and requires review in the Work Order Center; once approved, the stock is successfully deposited.
    - If the transferred securities are physical shares, the operator may manually set an unfreeze time during processing; the physical shares will automatically unfreeze at the specified time. If no time is set, they will unfreeze immediately upon workflow approval.

- Approve (bulk operation available): After the processing result is submitted, an [Approve] button appears in the action column; selecting it opens the Work Order approval page.
    <img src="/assets/S6KUbrtpto04xixMKjvjlQgbpSg.png" src-width="1280" src-height="671" align="center"/>
    - After processing, the workflow proceeds to the next node and requires review in the Work Order Center; once approved, the stock is successfully deposited.

- Submit Unfreeze (bulk operation available): If the client transferred physical shares and an unfreeze time was set during processing, but the client wishes to process the physical shares before the scheduled time, a manual unfreeze may be submitted. The submission requires another approval; once approved, the shares will be immediately unfrozen.

<img src="/assets/UTzYbUW8loMimfxntIUjjRFspFd.png" src-width="1280" src-height="651" align="center"/>

<img src="/assets/UFR0bMAsKod67TxnaUTjfYoopSd.png" src-width="1280" src-height="665" align="center"/>

### Deposit Restrictions

To improve the success rate of securities acceptance and prevent transfers of delisted stocks, transfer restrictions can be enforced in advance by setting a stock blacklist. The system provides both single-entry restriction and bulk restriction functions:

- Single-entry Restriction

<img src="/assets/Gt4zbQSnYobLcMxlwhxjh1W9pog.png" src-width="2988" src-height="1344" align="center"/>

- Bulk Restriction

Entry

<img src="/assets/BQkyb2AJGonvcOxN3o6jyCrdp9b.png" src-width="3016" src-height="1328" align="center"/>

Template

<img src="/assets/FPqHbjbT1obhArxwqFIj4oPCpqg.png" src-width="422" src-height="166" align="center"/>

### Email Sending Records

After the user notifies the broker of the target deposit application, the corresponding email records will be saved for subsequent issue tracking.

<img src="/assets/Vb7vbIDJQoHXA0xHiAvj4TZ3pGL.png" src-width="2928" src-height="1340" align="center"/>

