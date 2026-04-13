---
title: Quick Start
slug: UbQ2wCsRyiWNrpknpa3ccCvunac
sidebar_position: 1
---


# Quick Start

# Overview

Whale's funds management system provides deposit capabilities for multiple scenarios. Operators may submit clients' deposit applications, approve deposits, track exception records during the deposit process, and query all historical records within the system.

# Quick Start

Based on actual business requirements, the deposit function includes two types: application-based deposit or bank statement-based deposit.

# Prerequisites

Operators should obtain the following system permissions to access and use deposit-related functions.

<table header_row="1">
<colgroup>
<col width="275"/>
<col width="393"/>
</colgroup>
<thead>
<tr><th><p>Permission Name</p></th><th><p>Permission Description</p></th></tr>
</thead>
<tbody>
<tr><td><p>Permission to manage fund parameters, bank statements, and deposits</p></td><td><p>Permission to manage bank statements; deposit and withdrawal records/methods; bank cards; foreign exchange operations; funding guidelines; and fund parameter configuration</p></td></tr>
</tbody>
</table>

# Deposit Configuration

# Fund Parameter Configuration

## 1. Company Bank Account

Before a client can deposit funds, the corresponding company bank account must be added in the back office, and the deposit methods supported under that company bank account need to be configured.

<img src="/assets/Lgaqb4w6So4HpGxcDqgjeb6Qpbc.png" src-width="3772" src-height="1392" align="center"/>

<img src="/assets/OibdbZ9Zgoiescx87QLjzwj2pzW.png" src-width="2584" src-height="2372" align="center"/>

## 2. Currency

Deposit currencies must be configured in the system before clients can initiate deposits.

<img src="/assets/IkWQbiV4poXDFnxuVjNjMaOcpRh.png" src-width="3834" src-height="1317" align="center"/>

# Client Bank Card

Clients must configure their bank card information with the broker.Bank cards can be added either by the clients via the client app or by back office operators.

<img src="/assets/XFAmbhrDjovTE0xVDNSjFNQNpyb.png" src-width="3816" src-height="974" align="center"/>

Add a single card

<img src="/assets/XKUubsOoNoaYDExGTkyjxMFJp0c.png" src-width="3252" src-height="2832" align="center"/>

Bulk addition

<img src="/assets/QNPwbIit3oToeTxhMevjxIySp3e.png" src-width="1692" src-height="1770" align="center"/>

# Bank–Securities Account Opening

If a client intends to deposit via bank–securities transfer, a bank–securities account opening is required. If the client has submitted a bank–securities account opening request, the corresponding record can be viewed in the back office.

<img src="/assets/VBLQbVpj4ovY5Qxy43CjlLW7p5d.png" src-width="3284" src-height="1078" align="center"/>

# eDDA Authorization

If a client intends to deposit via eDDA, eDDA authorization is required. Once the client completes eDDA authorization, the corresponding record can be viewed in the back office.

<img src="/assets/Jzhjb7tg7o8HB1xSnfaje3Yepff.png" src-width="3292" src-height="1268" align="center"/>

# Bank-Related Information Configuration

The enumeration values used when setting up client or company bank account information—including common banks, countries/regions, and bank regions—can all be configured through the back office.

## 1. Card-Issuing Bank

<img src="/assets/QcKgbW46YoRpkHx2ikZjV5h6p5e.png" src-width="3292" src-height="1254" align="center"/>

## 2. Client Card Binding – Country/Region

<img src="/assets/XH5jb43AGoH7m7xcq7pjU7MypYc.png" src-width="3288" src-height="1086" align="center"/>

## 3. Bank Region List

<img src="/assets/AL0TbJn2No536nxplq0juz4Dp4c.png" src-width="3286" src-height="1246" align="center"/>

# Deposit Operations

# Deposit Process for Clients with Opened Accounts

## 1. Application-Based Deposit

## 1.1 Create a Deposit Application

A deposit application is a prerequisite for processing a client deposit. It records client information, client bank card, receiving bank, deposit amount, deposit currency, and supporting document. Applications can be created in one of two ways: submitted directly by the client through the client app, or created by a back office operator based on the client's instructions.

1. Querying client-submitted deposit applications

<img src="/assets/BHjsbsmfZoZvJHx8OwSjrVw0pfe.png" src-width="3810" src-height="1238" align="center"/>

1. Manual creation by back office operators

Back office operators create deposit applications manually according to the client's instructions.

Select the client and enter information such as the bank, deposit method, deposit amount, deposit currency, supporting document, and remarks.

<img src="/assets/PWrebiVInoZua5x8W90jFuSXpyd.gif" src-width="2086" src-height="994" align="center"/>

## 1.2 Process the Deposit

After receiving a deposit application, Back office operators can process the deposit using one of the two methods: Direct Deposit or Voucher Association.

1. Direct Deposit

The back office operator locates the corresponding application within the deposit application page, verifies the information, and initiates funding directly.

Click Credit directly in the action column, and in the pop-up window, confirm the following:

- That all application details are correct.
- Bank statement information corresponding to the application. If the statement is not yet available, the application can still be submitted for approval, and the statement details can be supplemented later.

<img src="/assets/Xyk0bjCzFoINt0xngEdjmuYbp8c.png" src-width="3814" src-height="1770" align="center"/>

- When the deposit method is cheque, the operator may choose to freeze the funds based on actual business requirements. If the operator selects Yes under Do check deposits need to be frozen, the operator can manually specify the Estimate thawing time.

<img src="/assets/I1ruboUtxoXTkBxmq7mjDmBbpoH.png" src-width="3334" src-height="1770" align="center"/>

1. Voucher Association

- When multiple applications need to be processed at once, the operator can go to the Vouchers associated page for batch funding.

<img src="/assets/GQhObxAOdoPRuPx1B6NjR09FpZf.png" src-width="3316" src-height="1212" align="center"/>

- On the Vouchers associated page, all applications pending deposit will be displayed automatically. The operator can review, select, and submit applications for funding.

<img src="/assets/Jp96bpjedoZHmPxhYWIjUsYtpYd.png" src-width="2404" src-height="1134" align="center"/>

- When the deposit method is cheque, the operator may choose to freeze the funds based on actual business requirements. If the operator selects Yes under Do check deposits need to be frozen, the operator can manually specify the Estimate thawing time.

<img src="/assets/CqkBboHyFoabEIxVT1oj4fGzprc.png" src-width="2454" src-height="1352" align="center"/>

## 1.3 Deposit Review

Enter the Deposit Review tab, locate the relevant record, and click Audit to trigger the work order. The deposit will be credited after approval.

<img src="/assets/D018bCNMmoIHhCx5rryjOGdvpgc.png" src-width="3280" src-height="754" align="center"/>

<img src="/assets/ZpDsbrgsEo6f82xhRAFjVxK4pBf.png" src-width="3310" src-height="1960" align="center"/>

<img src="/assets/ZwEabxUNbo1iymxk5GMjNI5ZpBh.png" src-width="3264" src-height="954" align="center"/>

- If multiple records require approval, they can be selected and approved in batch.

<img src="/assets/QMQZbcGrbocGj6xmFmxjqP50pGf.png" src-width="3398" src-height="1836" align="center"/>

- During deposit review, when the deposit method is cheque, information on whether the deposit needs to be frozen will be displayed.

<img src="/assets/Grx5bKTaCowKFExtU0njruVtpbP.png" src-width="3300" src-height="1738" align="center"/>

## 2. Bank Statement-Based Deposit

This workflow processes deposits based on funds actually received by the bank.

## 2.1 Obtain Receipt Information

Receipt information is available in two forms: deposit statements and bank instant messages.

1. Deposit statements

After funds are received, the system can directly obtain the bank statement via the bank API.

<img src="/assets/KndmbcUoUo6yO8xybSTjqH2TpBe.png" src-width="3778" src-height="738" align="center"/>

If a bank API integration is not in place, statements may be imported manually in the back office using the online banking template.

<img src="/assets/MCDIbLwTBodeHkxy8t9j585tpRf.png" src-width="3290" src-height="842" align="center"/>

<img src="/assets/IdcubZM9GoaEwOxsl7gjUN0Opvc.png" src-width="3306" src-height="1766" align="center"/>

<img src="/assets/PKL2bOTHGoHWr0xsTYvjYYtipjc.png" src-width="3308" src-height="1768" align="center"/>

<img src="/assets/NKtsb7hJHoHQWPxaDwUjn7fspEc.png" src-width="3314" src-height="1760" align="center"/>

1. Bank instant messages

For bank-securities transfers and eDDA deposits, the bank sends an instant funding notification via API upon successful receipt. The system captures this automatically, matches the relevant client, and processes the deposit without any manual intervention.

## 2.2 Manual Association

For bank statements imported manually, manual association is required. This includes two scenarios: associating with a deposit application and associating with a bank card.

1. Associate with a deposit application

- This applies to clients who already have an account and have submitted a deposit application, and account-opening deposits where the verification type is set to transfer verification.

Step 1: Select the bank statement record and click Link to enter the secondary page.

<img src="/assets/RGIob9fcXoIaZZxSOWZj7BFJpSh.png" src-width="3282" src-height="1100" align="center"/>

Step 2: On the secondary page, link the selected bank statement record to the corresponding deposit application. After confirming the reconciliation results on the page, click Link. The record will then be routed to the approval stage.

<img src="/assets/MHnDbcbkvodBMLxIgb3jNcnHpge.png" src-width="3288" src-height="1748" align="center"/>

- When the deposit method is acheque, the operator may choose to freeze the funds based on actual business requirements. If the operator selects Yes under Do check deposits need to be frozen, the operator can manually specify the Estimate thawing time.

<img src="/assets/OA17buBjgoKBjkxty0SjzEsEpDe.png" src-width="3276" src-height="2528" align="center"/>

1. Associate with a bank card

If the client did not submit a deposit application and the back office operator did not create one, the bank statement entry can be associated directly with the client's bank card for funding

<img src="/assets/KmFlbOYvKoKNVqx2NhFjzR9Upof.png" src-width="3302" src-height="2376" align="center"/>

1. Directly associate with a securities account

This applies to clients who already have an account and have not submitted a deposit application, and account-opening deposits where the verification type is set to cheque verification.

Bank statement entries can be directly associated with the securities account for funding.

<img src="/assets/Y4Jsb2Hc3oUVWlx7Kzyj3mF9pQg.png" src-width="3212" src-height="1766" align="center"/>

## 2.3 Deposit Review

For specific operations, see "1.3 Deposit Review".

# Deposit Process for Clients During Account Opening

- If the client has selected transfer verification as the verification type, the deposit must be processed through a deposit application. For details, see "1. Application-Based Deposit".
- If the client has selected cheque verification and did not submit deposit application from the client app, the deposit must be processed based on the bank statement. For details, see "2. Bank Statement-Based Deposit".

In cases where the deposit has already been approved but the client's account opening is still in progress, the following steps apply:

Step 1: Enter the Account Opening Deposit tab. This tab displays deposits that have been approved and are pending account opening completion.

<img src="/assets/Dc6ubL713odrTAxscyIjV8Dip7b.png" src-width="3246" src-height="1094" align="center"/>

Step 2: Monitor the Account Opening Status and Deposit Status columns. If a client's account opening ultimately fails, the Account Opening Status will show Approval Failed.

<img src="/assets/LgWhbGggfo48vWxwZ7pj1W5Npqd.png" src-width="3276" src-height="1226" align="center"/>

Step 3: Select the deposit record for the client whose account opening failed and click Reject. The deposit process must then be restarted from the beginning.

<img src="/assets/GQ2wbsCn0ovROIxrpl6jeQ1dpY9.png" src-width="3276" src-height="1226" align="center"/>

