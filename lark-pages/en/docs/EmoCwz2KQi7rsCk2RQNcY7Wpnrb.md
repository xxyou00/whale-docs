---
title: System Overview
slug: EmoCwz2KQi7rsCk2RQNcY7Wpnrb
sidebar_position: 1
---


# System Overview

This user manual applies to the Longbridge Whale — Entitlements Platform and is intended for operations system administrators and authorized users. By reading this manual, you will learn how to operate the Whale Entitlements Platform.

The Entitlements System is Whale’s solution for managing the distribution of various marketing rewards and entitlements, including creation and issuance of a variety of coupons and rewards. Within the Whale Entitlements System, the primary functional areas are Coupon Benefits, Rewards Center, and Entitlements Center.

<img src="/assets/UTpSbqoZgoRnLTxuGyPjyDtwpvb.png" src-width="2708" src-height="828" align="center"/>

# Feature Overview

# Entitlements Workflow

Intended users: operations personnel. The Entitlements System involves the following parties:

- Entitlements System: operations personnel are responsible for configuring and managing entitlements projects (Coupon Benefits / Rewards Center / Entitlements Center).
- App Client: end users who interact with various entitlements.
- Settlement System: responsible for the financial processing generated when customers interact with entitlement projects.
- Data Service System: refers to cases where certain entitlements relate to market data service activation (if applicable).
- Trading System: refers to cases where certain entitlements relate to trading services (if applicable).

<img src="/assets/T9c2bSbN0oynMGxfp8Wjd9uOpUe.png" src-width="1046" src-height="2644" align="center"/>

# 1. Coupon Benefits

## 1.1 Menu Structure

## 1.2 Coupon Configuration

Navigation: Operations System &gt; Entitlements System &gt; Coupon Benefits &gt; Coupon Configuration

<img src="/assets/V7fib0G6SotzltxkzzTjk1JMp5g.png" src-width="1553" src-height="719" align="center"/>

List operations:

- Query: Filter and search existing coupons by product template code, title, coupon type, validity period, etc.
- View: Click View to see all configuration fields for the selected coupon.
- Edit: Click Edit to modify the coupon fields and rules — use caution; saved changes may affect coupons already issued and in production.
- Copy: To rapidly create a similar coupon, click Copy to duplicate the current coupon template and then modify selected fields to create a new coupon quickly.

### 1.2.1 Create New Coupon

This function provides a tool for creating new coupons. After creating a coupon and obtaining the reward template code, the coupon can be issued via the activity system or other distribution methods.

The current Whale Entitlements System supports configuration of the following coupon types:

Operation details:

Click the “New” button at the top-right to open the creation page. Coupon information is divided into Basic Information and Rule Configuration. Basic Information fields are common across coupon types; Rule Configuration fields vary by coupon type.

<img src="/assets/OdJyb1i68oVfvMxxfmljKXLxp7d.png" src-width="874" src-height="860" align="center"/>

Basic Information:

Select the coupon type to create; the Basic Information fields are the same for all coupon types.

Rule Configuration:

After selecting the coupon type to create, configure rule fields specific to that type, as described below.

After completing these configurations, click Confirm to generate the coupon and reward template code.

### 1.2.2 Coupon Management

Navigation: Operations System &gt; Entitlements System &gt; Coupon Benefits &gt; Coupon Management

This function provides viewing of coupon issuance records. The list displays each issuance record for every coupon, regardless of issuance channel.

Filter and export by coupon number, reward template code, coupon type, issuance time, customer ID, coupon status, and other criteria.

<img src="/assets/LqmAbVZ3top7UAxHR45jnnvcpLM.png" src-width="1514" src-height="727" align="center"/>

### 1.2.3 Coupon Settlement

Navigation: Operations System &gt; Entitlements System &gt; Coupon Benefits &gt; Coupon Settlement

This function provides viewing of coupon settlement records and is applicable to coupons that result in cash refunds (Commission-Free Coupons and Stock Cash Back Coupons).

The list contains each cash-back record; every successful cash-back is considered a settled record.

Filter by coupon number, user ID, settlement date, activity code, redemption scenario, etc.

<img src="/assets/N6vgbKPOgoHV95xU6Aljx0rnpWe.png" src-width="1703" src-height="400" align="center"/>

## 1.3 Physical Prizes

Navigation: Operations System &gt; Entitlements System &gt; Coupon Benefits &gt; Physical Prizes

<img src="/assets/ENDWbdk76oSzajxGuKJjmr26p8b.png" src-width="3420" src-height="658" align="center"/>

List operations:

- Query: Filter by prize template code, prize type, creation time, etc.
- View: Click View to see all configuration fields of the selected physical prize.
- Edit: Click Edit to modify the prize information.
- Copy: Click Copy to duplicate an existing prize and modify fields to create a new prize quickly.

### 1.3.1 Create New Physical Prize

Click the “Create Template” button at the top-right to open the creation page.

<img src="/assets/H5W7bGAbsoI14KxjZX2jOQLSp2b.png" src-width="555" src-height="832" align="center"/>

Configure the following fields:

After completing these fields, click Submit to create the template; the system will automatically generate a prize template code.

### 1.3.2 Physical Fulfillment Management

Physical fulfillment workflow:

<img src="/assets/CbtnbLA9VoxI7Fx19B2jW0Orppe.png" src-width="632" src-height="1088" align="center"/>

Navigation: Operations System &gt; Entitlements System &gt; Coupon Benefits &gt; Physical Fulfillment Management

This function supports combined online and offline operations to ship physical rewards to recipients and provides querying of fulfillment records.

Fulfillment operation instructions:

After a user receives a physical reward, a record is created in Physical Fulfillment Management. Once the user supplies a shipping address via the mobile app, fulfillment must be executed as follows:

(1) Filter users who have filled in their address

<img src="/assets/InLIb29mboODMQxsgvFjL5cupOc.png" src-width="1562" src-height="526" align="center"/>

If a user has not provided an address, the fulfillment status will be “Address Not Provided.” Once the user provides an address, the status changes to “Address Provided.” Use this filter to find records that are ready for shipment.

(2) Export addresses

After filtering for users who have provided addresses, export the address information to proceed with offline shipment.

<img src="/assets/E790bLCWMobsw8xmnVqjaxeKphe.png" src-width="1598" src-height="494" align="center"/>

To prevent address changes after export, lock the record status. After exporting, batch change the fulfillment status to “Shipping In Progress”; once set, the user can no longer modify the address.

<img src="/assets/Wq8tb36aeoOxgZxg0VQjSKPFpQf.png" src-width="1603" src-height="515" align="center"/>

(3) Upload tracking numbers

After shipping offline, collect tracking numbers and enter them into the system so users can view shipment tracking.

If there are only a few tracking numbers, enter them individually by clicking the “Ship” button for each record and inputting the tracking number in the dialog.

<img src="/assets/RpdKbuaehozgTmxzsQSjL62ppwb.png" src-width="1551" src-height="598" align="center"/>

For large volumes, use “Batch Import Tracking Numbers” at the top-right to bulk import tracking numbers via file upload.

<img src="/assets/Aq7vb2DxcoqUeExdx8VjpHiMpxH.png" src-width="1562" src-height="601" align="center"/>

After uploading tracking numbers, the physical reward fulfillment process is complete.

# 2. Rewards Center

The Rewards Center consolidates reward issuance records from various distribution channels and supports manual reward issuance and approval workflows for user asset redemptions.

## 2.1 Reward Issuance

This section provides querying of all issued reward records and manual reward issuance functions.

### 2.1.1 Query Reward Records

Navigation: Operations System &gt; Entitlements System &gt; Rewards Center &gt; Reward Issuance

<img src="/assets/NHlvbqDPOosoWnx8FjkjnspYpnb.png" src-width="1558" src-height="368" align="center"/>

### 2.1.2 Manual Reward Issuance

Applicable scenarios: For non-standard activities or special cases where no automated rules exist—such as issuing a gift to a loyal customer or correcting omissions in online activities—the manual issuance function is used.

Issue to a single user:

Click the “New” button at the top-right to open the issue dialog.

<img src="/assets/GROKbJPRGomfEpxKcIQjJXyUpAg.png" src-width="2764" src-height="310" align="center"/>

<img src="/assets/DpkubNq2JoxVnSx9vy0jpTo0pWb.png" src-width="1564" src-height="856" align="center"/>

After confirming, the issuance record is created. If an approval workflow is configured, the record enters the approval flow and will be issued upon approval; if not approved, the issuance is canceled. If the approval flow is automatic, the record is issued immediately.

Issue to multiple users:

For bulk issuance, click “Batch Issue Rewards” at the top-right and upload a file to issue rewards to multiple users at once.

<img src="/assets/NN7Ob8k6toFqIoxWEsmjt1JqpCe.png" src-width="1598" src-height="262" align="center"/>

<img src="/assets/VFVrbmbpToFaKax7bHGjEjmSpzg.png" src-width="1569" src-height="857" align="center"/>

First select the reward type, then download the template file from the template section (different reward types require different templates; follow the steps in order). Complete the template file and upload it by dragging it into the input box. After confirming, the system generates the corresponding number of issuance records. Records will enter the approval flow if configured; otherwise they will be issued according to the approval configuration.

## 2.2 Asset Disposal

This function handles user assets (stocks and cash). When users receive cash, query records here; when users redeem coupons for stocks, perform approval operations here.

Users may redeem Stock Coupons to receive corresponding shares, or accumulate multiple Stock Cash Back Coupons until their combined value reaches at least one share price, at which point they can be redeemed together for a share.

Navigation: Operations System &gt; Entitlements System &gt; Rewards Center &gt; Reward Issuance

<img src="/assets/DapYbh9stojxodxlpjvjs5Gvpom.png" src-width="3412" src-height="646" align="center"/>

Cash and cash coupons are generally issued directly. For stock redemptions, approval is required here before the corresponding shares are transferred to the recipient’s account.

# 3. Entitlements Center

The Entitlements Center is currently used for managing market-data products and for viewing/exporting orders generated by the Market Data Shop.

## 3.1 Entitlements Shop

Navigation: Operations System &gt; Entitlements System &gt; Entitlements Center &gt; Entitlements Shop

<img src="/assets/EWAKbBBB4oSQmGxVR1cjPLQvpfc.png" src-width="3420" src-height="1254" align="center"/>

If you subscribe to Whale’s content services that include market data, you may sell market data viewing permissions to users as market-data products. Whale staff will assist each tenant in creating and managing market-data products; further details are not covered here.

## 3.2 Entitlements Orders

Navigation: Operations System &gt; Entitlements System &gt; Entitlements Center &gt; Entitlements Orders

This function is used to query and export orders generated by the Market Data Shop for operations and finance personnel.

<img src="/assets/IHU7b7O4mo0LEUxF8l9j7Cijpjh.png" src-width="1594" src-height="611" align="center"/>

# App Client Features

The following demonstrates how configurations are presented in the front-end app.

## Coupons

App Entry:

<img src="/assets/BNKLbxaCrobUrQx2oi9j60PqpSb.png" src-width="608" src-height="1262" align="center"/>

My — My Coupons

My Coupons:

<img src="/assets/SxDxbvBJiotKj3xaZGEjKDL8pVb.png" src-width="675" src-height="1403" align="center"/>

Users can view their current coupons and coupon statuses.

Using Coupons in Trading:

<img src="/assets/YU1lb6tpwo11gVx4f1QjsYq5p1f.png" src-width="564" src-height="1242" align="center"/>

<img src="/assets/SIKWbnxyyoyTIhxFRrRj1Ealpub.png" src-width="1170" src-height="2532" align="center"/>

Using Coupons for IPO Subscriptions:

<img src="/assets/NNNcbmIGRoKTTQx0nv1jnOPPpqc.png" src-width="1290" src-height="2796" align="center"/>

## Rewards

App Entry:

<img src="/assets/JIocbGjeQoQt7vxlcZ6jH1Meprf.png" src-width="600" src-height="1252" align="center"/>

My — Reward Records

<img src="/assets/TAogbTkqGow9jSxTkLKjwy6Zpyh.png" src-width="542" src-height="1178" align="center"/>

Reward Records:

<img src="/assets/WIVkbCcwDod6KuxNAdqj2vRjpWe.png" src-width="1170" src-height="2532" align="center"/>

Displays all historical records.

<img src="/assets/TY3nbtPGfoIcybxeO34jWI9Jpkg.png" src-width="1170" src-height="2532" align="center"/>

Filter by category to view specific records.

Physical Reward Claiming:

<img src="/assets/PZJ9bOnahoZiOexJecljLD2LpKe.png" src-width="560" src-height="1222" align="center"/>

Enter address and phone number.

<img src="/assets/UoTXbWlxWoDBHMxdjtJjc9qBp1g.png" src-width="536" src-height="1168" align="center"/>

Confirm shipping information.

<img src="/assets/ZRSibqWkgoAW3JxvEAIjIgY3pAe.png" src-width="554" src-height="1202" align="center"/>

View logistics/tracking number.

## Entitlements Shop

Shop Entry:

<img src="/assets/GPU4bSornoME0PxTC8rj6atIpyb.png" src-width="1196" src-height="2488" align="center"/>

<img src="/assets/RTjObKbXGoWuTpxEQCBjTSg5pIb.png" src-width="536" src-height="1264" align="center"/>

My — My Market Data — Market Data Shop

Market Data Shop:

<img src="/assets/OwKEbPVcCoQlwDxAhl6jy9VFpwd.png" src-width="1290" src-height="2796" align="center"/>

Displays all products; tabs allow switching between product lists for different market data.

Purchasing a Product:

<img src="/assets/P288b6IkwooTuBx37wDjRBU0pEh.png" src-width="1290" src-height="2796" align="center"/>

Select the appropriate product and package, then proceed to payment.

Viewing Purchase Records:

<img src="/assets/ETjkb3zO0oGimCxFvBVjnJPPpme.png" src-width="587" src-height="1227" align="center"/>

<img src="/assets/CEYebwVofop87uxfmxvjUzd1pIh.png" src-width="377" src-height="774" align="center"/>

