---
title: System Overview
slug: T15Awmt9Vi8QbCk5nJcjUpXRp9c
sidebar_position: 1
---


# System Overview

The Activity System is the core marketing campaign management module provided by the Whale OPA operations system. It enables broker tenants to manage various marketing campaigns by offering configuration and management capabilities. The system currently supports the following activity type groups:

- Standard activity types: referral activities / basic activities / team activities, etc.
- Non-standard activity management: provides customizable activity management elements to accommodate personalized campaigns.

Manage diverse campaigns using convenient marketing templates to achieve digital marketing.

<img src="/assets/XlDobYRVMo1nOkxWOjNjpgDEpkg.png" src-width="1280" src-height="945" align="center"/>

## 1. Features

### 1.1 System Architecture

<img src="/assets/FUWfbI8OBoQFKzxQu38jgHGrpQf.png" src-width="1280" src-height="729" align="center"/>

### 1.2 Achievement Task Types and Descriptions

### 1.3 Reward Types

When creating an activity, three reward types can be set: physical items, vouchers, and cash.

Refer to the Rights System documentation for instructions on creating physical items and vouchers.

### 1.4 Activity Configuration Process

Applicable personnel: operations staff. The activity system involves the following parties:

- Activity System: Operations staff are responsible for configuring and managing online activities.
- User Segmentation: Defines target users and obtains asset-related data during the activity.
- Rights System: Associates relevant activity rewards.

<img src="/assets/CwKzbRBj1oZoScxBes6jdxL3pUc.png" src-width="1280" src-height="511" align="center"/>

## 2. Standard Activity Management

Navigation: Operations System &gt; Activity System &gt; Standard Activity Management

This operation allows maintenance and management of standard activities.

- Upper level: choose an activity template to create an activity.
- Lower level: query and manage records of created activities.

<img src="/assets/MkZGbIW1doSjfQx8TGHjfTNtprc.png" src-width="1280" src-height="546" align="center"/>

Activity management list field descriptions

### 2.1 Referral Activities

#### 2.1.1 Referral Activity Business Logic

If any activity page has a sharing function configured, when a user shares that page and a new user registers via the share, an invitation binding is created.

Referral activities issue rewards based on the binding relationship.

<img src="/assets/VYvobSZmAoX9iWxSTUkjli7dpq6.png" src-width="1280" src-height="470" align="center"/>

Referral activities support two reward types: fixed rewards and tiered rewards.

- Fixed reward: For each invited user who completes the task, the inviter receives a fixed reward.
- Tiered reward: Divide the number of invitees into ranges. For invite counts within a range, each invited user yields the reward corresponding to that tier. When moving to the next tier, you may configure additional rewards for the inviter. Typically, higher invite counts correspond to larger rewards.

#### 2.1.2 Referral Activity Configuration

Navigation: Operations System &gt; Activity System &gt; Standard Activity

To add a new referral activity, click the "New" button under the Referral Activities module.

<img src="/assets/ZgnjbJS7CoKceExUzfXjLBv1pFD.png" src-width="1280" src-height="541" align="center"/>

The referral activity creation page:

<img src="/assets/PqWbbggmEoSxpWxxBu6jN6MZpSc.png" src-width="1194" src-height="1280" align="center"/>

Configure template fields as follows:

Reward Rules

Click to add a reward rule. Required fields vary by reward type and activity attribute.

Fixed reward:

<img src="/assets/UpBlbRrCLowcqQxP3Rhjsc73pbg.png" src-width="1280" src-height="877" align="center"/>

Tiered reward:

<img src="/assets/RIxCbgCZNoZZBYx8RETj001np0g.png" src-width="1280" src-height="907" align="center"/>

Note: Once filled, do not switch activity type or reward type arbitrarily, as this may clear configured lists.

Prize Settings

Click to create a prize rule. This section provides configuration options to limit how many times each user may receive a given prize.

<img src="/assets/FOxabgneVosY8TxZSsBj7Gn7p4e.png" src-width="1280" src-height="224" align="center"/>

#### 2.1.3 Referral Activity Reward Data Query

Data appears only when the activity is running and rewards are being issued.

Click the Details button for the corresponding activity, then open the "Winners" tab to access the following page:

<img src="/assets/V1g9bxd3botEXnxxgbBjNMDspnf.png" src-width="1280" src-height="269" align="center"/>

Data categories:

- Pending Submission: Reward records that have not had issuance requests submitted.
- Issuing: Reward records currently being issued.
- Issued: Reward records successfully issued.
- Failed: Reward records that failed issuance.
- Cancelled: Reward records for which issuance was cancelled.
- Locked: If the activity’s achievement task has a lockup configured, this shows the number of reward records currently in lockup.
- All: Total reward records for the activity.

### 2.2 Basic Activities

#### 2.2.1 Basic Activity Business Logic

<img src="/assets/RZHZbPbo8oTUxixuSnSjk0vMpac.png" src-width="1280" src-height="460" align="center"/>

#### 2.2.2 Basic Activity Configuration

Navigation: Operations System &gt; Activity System &gt; Standard Activity

Click the "New" button under the Basic Activities module.

<img src="/assets/Wi34bHfonoCN3Xx1GfgjRj0vpAd.png" src-width="1280" src-height="375" align="center"/>

Open the following page:

<img src="/assets/X61sb14Hzo8kIaxMsqNjGRmbpru.png" src-width="1280" src-height="936" align="center"/>

Configure template fields as follows:

Reward Rules

<img src="/assets/RWWpbzeeNoYCfAxKW5zjNyFGpTb.png" src-width="1280" src-height="808" align="center"/>

- Reward calculation logic varies slightly depending on the reward generation timing.

- For transaction or asset-based tasks, multiple tiers with multiple rewards can be configured by adding multiple reward rules.

Example: The following shows one activity with four reward rules. The net deposit task is split into three tiers; selecting "Real-time Generation" creates a reward record each time a user meets a tier.

<img src="/assets/KolTbRU4voZn57xxeXzjeVI4pSc.png" src-width="1280" src-height="467" align="center"/>

#### 2.2.3 Basic Activity Reward Data Query

Reward data is available only when the activity is running and rewards are being issued.

Click Details for the relevant activity and open the "Winners" tab to view:

<img src="/assets/Y2iLbucvGoj51XxFiwxjYq3Ypqb.png" src-width="1280" src-height="271" align="center"/>

Data categories:

- Pending Submission: Reward records that have not had issuance requests submitted.
- Issuing: Reward records currently being issued.
- Issued: Reward records successfully issued.
- Failed: Reward records that failed issuance.
- Cancelled: Reward records for which issuance was cancelled.
- Locked: If the activity’s achievement task has a lockup configured, this shows the number of reward records currently in lockup.
- All: Total reward records for the activity.

## 3. Non-Standard Activity Management

Intended users: Operations staff

Use case: Offline prize distribution (e.g., VIP client rewards) where there are no explicit activity rules and the goal is to simply issue rewards.

Primary function: Create an activity to obtain an activity code; subsequently associate the activity code in the Rights System — Reward Center to issue rewards.

Navigation: Operations System &gt; Activity System &gt; Non-Standard Activity Management

You can query and manage created activities. (Note: standard activities are also archived in this list; thus, this list serves as a comprehensive activity repository.)

<img src="/assets/QZMSbhrLmoeaDGx6RSqjg6iBpde.png" src-width="1280" src-height="292" align="center"/>

Activity management list field descriptions

### 3.1 Non-Standard Activity Configuration

Click the New button at the top of the page to open:

<img src="/assets/A0LGbXPeFobgmIx28BkjfWO9pAO.png" src-width="1237" src-height="1280" align="center"/>

Because non-standard activities do not have explicit rules, creating them is mainly to obtain the activity code. Subsequent reward issuance is associated with this activity code in the Reward Center. Optional fields on the creation page may be left blank.

Important fields:

## 4. Referral Relationship Management

[Not Support block type: Diagram/21]

As shown: a user under an app generates a unique invite code for that app. When the user shares the invite code and a friend fills it in, the binding is recorded in the referral relationship list.

Referral relationships created via activity sharing can be queried here and may also be manually bound.

Navigation: Operations System &gt; Activity System &gt; Referral Relationship Management

<img src="/assets/TRQgbiJzjoXoVWxlKC6j6GXzpye.png" src-width="1280" src-height="395" align="center"/>

Primary functions:

- Query: Use the top tabs to query registration invites, account-opening invites, and deposit invites separately.
- Add: Manually bind referral relationships for users from the backend.
- Details: View detailed binding information, including binding channel and binding time, and modify the binding relationship.

(For already completed actions, the corresponding inviter for that node cannot be bound; for incomplete nodes, the inviter can be bound or changed.)

### 4.1 Add Referral Relationship

#### 4.1.1 Add Registration Referral

Click the New button in Referral Relationship Management to open the dialog:

<img src="/assets/JZwubvM7MoOsNRx2lW9jsF4Opyr.png" src-width="1280" src-height="120" align="center"/>

<img src="/assets/JxwNbPbSSosUCmxruEfjMPpTpWc.png" src-width="764" src-height="696" align="center"/>

Enter the invitee and inviter customer IDs to complete the binding.

#### 4.1.2 Add Account-Opening or Deposit Inviter

First, locate the invitee user you want to bind to by searching, then click the user’s details to view:

<img src="/assets/MnKsbDcMZoHQvpxH8zLjCjZZpZc.png" src-width="1280" src-height="142" align="center"/>

The details view shows the user’s registration inviter and allows binding of account-opening and deposit inviters.

<img src="/assets/Hhrjbj5PFozPPoxdZiCjp7vmpSc.png" src-width="1280" src-height="542" align="center"/>

In the pop-up, input the inviter’s user ID to bind the account-opening or deposit inviter for the invitee.

If the user has not completed a given node, you may change the inviter for that node using the same flow—enter the new inviter’s user ID to perform the change.

## Frequently Asked Questions for Operations

Q: When a user reports not receiving a reward, how should operations investigate?

Navigation: Operations System &gt; Activity System &gt; Standard Activity Management

First verify that the activity configuration is correct. Click Details for the activity and review the configured rules and rewards.

<img src="/assets/NLMVbnUfkoFX1HxrBL5j1YBxpVe.png" src-width="1280" src-height="171" align="center"/>

<img src="/assets/Q4J9byRWloYKhuxchusjLmkTp6L.png" src-width="1280" src-height="559" align="center"/>

If configuration is correct, verify the Winners list to see whether a reward record was generated and check the reward record status.

<img src="/assets/Pm1rbTXuHoDp46xxEWbjdbXfpHc.png" src-width="1280" src-height="263" align="center"/>

If status is Issuing, the system is still processing issuance. If Pending Submission, operations staff must click Submit to issue the reward.

Q: How to check whether a user's referral binding succeeded?

Navigation: Operations System &gt; Activity System &gt; Referral Relationship Management

<img src="/assets/NZFvbInruoWw1lxb091jkHH4p7g.png" src-width="1280" src-height="153" align="center"/>

After searching, the list shows all referral bindings for the user. Click Details to view the specific bound user information.

<img src="/assets/Qhynb3sm3oVJZQxD5tdjmiyupFh.jpeg" src-width="1280" src-height="395" align="center"/>

<img src="/assets/UHDEbYtZzoDmS4xSChJjtSJ5pxc.png" src-width="1280" src-height="536" align="center"/>

