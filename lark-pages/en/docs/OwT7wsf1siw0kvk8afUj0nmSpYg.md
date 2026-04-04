---
title: System Introduction
slug: 2a05bab0c2cc818c8cade6f552896fe8
sidebar_position: 2
---


# System Overview

# 1. System Overview

This guide outlines the comprehensive back office operational workflow for cryptocurrency withdrawal services, encompassing record generation, query and tracking, and the work order approval process. It is intended to ensure standardized operations by back office operators and to maintain business compliance and fund security.

# Prerequisites

- The back office operator has logged in to WBO using dedicated credentials and navigated to VA Clearing Management &gt; Deposit & Withdrawal &gt; Withdrawal.
- The account holds the necessary permissions for operations such as withdrawal application and approval. Operators who have not been granted the required permissions should contact the administrator to request access.

# 2. Operation Instructions

## Cryptocurrency Configuration

Operators should configure cryptocurrency settings for withdrawals before processing client withdrawals.

<img src="/assets/WxInbxzuvopUTlxQvZqjCs0wpWd.png" src-width="1280" src-height="614" align="center"/>

## Client Wallet Address

To ensure asset security, wallet address verification must be completed before a withdrawal is processed. This is a critical prerequisite step.

<img src="/assets/YC7KbmBeQoBUpexHy40jN3Cxpog.png" src-width="1280" src-height="610" align="center"/>

## Withdrawal Operations

<b>Request Reception and Record Generation</b>

<div class="callout callout-bg-5 callout-border-5 callout-color-1">
<div class='callout-emoji'>📍</div>
<p>Navigation: WBO &gt; VA Clearing Management &gt; Deposit &amp; Withdrawal &gt; Withdrawal Application</p>
</div>

- After the client submits a withdrawal request, the system automatically receives the request information and generates a unique deposit record (including record number, client securities account, deposit currency, amount, destination address, transaction hash (TXID), request time, status, and other core information).

<img src="/assets/FuAkbZimLopOVcxWTksj21uipsf.png" src-width="2468" src-height="602" align="center"/>

- Withdrawal applications submitted by clients are automatically linked to the WBO work order system (work order ID: atm.va.coin_withdraw_apply). The system will conduct the approval process based on the pre-configured approval workflow.

<img src="/assets/S7oubUN6Hoj8UsxWWiKjtyPapKf.png" src-width="2498" src-height="1324" align="center"/>

