---
title: System Introduction
slug: B0Bnw3jYFiN1HBkKUqFcYyMInWd
sidebar_position: 2
---


# System Overview

# System Introduction

# 1. System Overview

Securities transfer-out is a service in the financial system that allows investors to transfer their securities holdings from one account to another to achieve flexible asset allocation and management.

The Whale system includes functions such as transfer-out application, transfer-out details, and email notification to brokers. The process supports the review requirements of different roles and effectively reduces the risks during securities transfer-out. The overall process is as follows:

<img src="/assets/KgDUwdi7mhFjWCbA4kBjkfBSpQe-board.jpeg"/>

## Prerequisite

None

# 2.Operation Instructions

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: Stock Management &gt; Transfer Out</p>
</div>

## Transfer-Out Application

A transfer-in application is initiated by the client and consists of four components: broker information, account information, securities details, and remarks. Back office operators can create applications manually on a client's behalf, and may take the following actions on any submitted application: reject, submit for approval, or notify the delivering broker.

- Manual transfer-out: This applies when a client contacts a back office operator to request a manual transfer-out. The operator must enter the client's security details and account information.
    - After the operator selects a client, the system automatically populates all of the client's holdings. Then the operator selects the target records, checks the quantities to be transferred out, and confirms the transfer-out.

<img src="/assets/O7q0b0PINoFRusxRjs3jNt4vpHf.png" src-width="2994" src-height="1312" align="center"/>

- Reject (batch operation supported): If the transfer-out application submitted by a client contains an error or the back office operator deems the application invalid, the operator can click Reject.
- Notify Broker: Since transfer-out operations require cooperation from the delivering broker, in practice, operators need to contact the delivering broker to ensure a timely transfer-out. The Notify Broker function provides an in-system email tool that allows operators to send notifications to the delivering broker. Email delivery results are displayed to operators, giving them visibility into whether the broker has been notified.
    - Select the broker institution to which the email should be sent. The system will automatically populate the broker's email address. The operator should verify that the email address is correct.
    - Select the securities transfer-out application details under the target broker. (Already-sent application details will be excluded.)
    - Preview the email content, and click OK after confirming it is correct.
    - Go to the Email Records tab to check the sending status.

<img src="/assets/ZeI7bupM6ouP1wxXi6fjYnYUpOe.png" src-width="1280" src-height="572" align="center"/>

<img src="/assets/Pz6sbSR74oT1WZx6QFGj5AEvpWe.png" src-width="1280" src-height="567" align="center"/>

<img src="/assets/UvkbbEp9eoGlx2xo4BsjD8WGpoe.png" src-width="2996" src-height="1312" align="center"/>

<img src="/assets/QCKzbL88FopUWTxxQCZjAlYKppd.png" src-width="2976" src-height="1320" align="center"/>

- Submit (batch operation supported): Once the operator has completed a preliminary review and confirmed that the application contains no issues, click Submit to forward the application to the next-stage operator for further review and processing.
- Edit: If, while processing a transfer-out application, the operator receives updated information from the client regarding whether the delivering broker has been notified, click Edit to update the notification status accordingly. This ensures that the application record reflects the actual state of broker notification.

<img src="/assets/BZCMb3S8qozffhxxoyajEb94pXf.png" src-width="2984" src-height="1317" align="center"/>

- Indicator Cards

For brokers with high transfer-out volumes, the system provides categorized indicator cards for refined operations. The cards are arranged from left to right in alignment with the sequence of business operations. The available batch operations include:

<img src="/assets/RG8BbdWmho83DnxV6X5jFUoopJh.png" src-width="2954" src-height="1320" align="center"/>

## Transfer-Out Details

As a transfer-out application may contain multiple securities detail records, the operator responsible for processing the transfer-out must carefully review each record before the transfer-out can proceed.

- Edit: If the operator finds an issue with a specific detailed record submitted by the client when processing securities details, the operator can click Edit to correct the record after confirming with the client.
    <img src="/assets/OMqvb8doloaJJFxwa23j5AGWpdb.png" src-width="2958" src-height="1308" align="center"/>
    - Editable fields include the custodian code, sub-account number, securities detail quantity, and remarks.

- Modify Transfer Fees: Before transfer-out, the operator can choose whether to adjust the client's transfer fees and whether the modified information should be displayed to the client based on the actual business scenario.

<img src="/assets/MbD1bVnysoPJAsxAGvtjua5gpWQ.png" src-width="2988" src-height="1324" align="center"/>

<img src="/assets/AUQSbDFwoo2Ro1x9g9vjTcGHpde.png" src-width="2970" src-height="1379" align="center"/>

- Delete: If the client reports that a specific submitted detail record should no longer be included in the transfer-out, the operator can click Delete to delete the target record.
- Generate SI: Since securities transfer-out requires SI information to be entered into CCASS, operators can click Generate SI to have the system automatically compile and save the SI data as an uploadable file, eliminating the need for manual entry in CCASS. Generated SI files can be viewed and exported from the SI List section.

<img src="/assets/EY2Bb19nUonq4VxLdSgjOqGKpvh.png" src-width="2978" src-height="1479" align="center"/>

<img src="/assets/McMYbW4cEorUTfxqDT4j94gLpQf.png" src-width="2998" src-height="1310" align="center"/>

- Edit SI: The operator can click Edit SI to modify the generated SI file.

<img src="/assets/Ai38bHSWgo0bOQx8yBijKA2rpy3.png" src-width="2990" src-height="1509" align="center"/>

- Handle-Submit as Successful/Submit as Failed: Once the operator has verified that a detail record contains no issues, click Handle and select Submit as Successful. If issues are identified, select Submit as Failed.
    <img src="/assets/Qg0FbfThkoqM9TxwizbjItQKppe.png" src-width="2962" src-height="1323" align="center"/>
    - After processing, the workflow advances to the next node and requires review in the Work Order Center. Upon approval, the securities are successfully transferred in.

- Approve: After the processing result is submitted, an Approve button appears in the Action column. The operator can click Approve to enter the work order approval page.
    <img src="/assets/ODqjb3yfYov9zoxqRvjjui6Yp9d.png" src-width="2962" src-height="1312" align="center"/>
    - After processing, the workflow advances to the next node and requires review in the Work Order Center. Upon approval, the securities are successfully transferred in.

## Email Sending Records

After the operator notifies the broker regarding a target transfer-in application, the corresponding email record will be saved for subsequent issue tracking.

<img src="/assets/TQVpbYYAiovk11xjNFgjBclKp3f.png" src-width="2994" src-height="1312" align="center"/>

