---
title: |-
  **Reference Materials:** []  
  **User Question:** Position Management
slug: WeOHwwAVzihR6BkUohhjJ13bpkh
sidebar_position: 4
---


# **Reference Materials:** []  
**User Question:** Position Management

```http
---
title: Position Management
slug: L4caw5q4fiphmkk468ZjKQJCpAF
sidebar_position: 5
---

# Position Management

# System Overview

This manual provides standardized guidance for the end-to-end back-office operational workflow for fiat currency and cryptocurrency position management. It covers core operational steps such as position inquiries, allocation rule configuration, automatic allocation, and manual allocation. The purpose is to guide back-office operators in performing work in a standardized manner, ensuring business compliance and fund security while mitigating operational risks.

# Prerequisites

- Back-office operators must log in to the WBO back-office system using a dedicated account and password. After a successful login, they can access the following core modules: “Virtual Asset Management - Position Management,” “Payment Management - Bank Statements - Company Fund Allocation,” “Business Parameter Settings - Fund Parameters - Settlement Channel Accounts,” and “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration.”
- Operator accounts must be granted the relevant operational permissions in advance for “Position Management,” “Company Fund Allocation,” “Settlement Channel Accounts,” and “Fund Allocation Configuration.” If the account does not have the required permissions, promptly contact the system administrator to submit a permission request. Operations may be performed only after the permissions are enabled.

# <b>Operating Path and Permission Details</b>

- The following lists the permission names, corresponding operational permissions, and permission identifiers for each core module. Operators must perform actions according to their assigned permissions and are strictly prohibited from performing unauthorized operations.
    <table header_row="1">
    <colgroup>
    <col width="317"/>
    <col width="163"/>
    <col width="400"/>
    </colgroup>
    <thead>
    <tr><th><p>Operating Path</p></th><th><p>Permission Description</p></th><th><p>Permission Identifier</p></th></tr>
    </thead>
    <tbody>
    <tr><td rowspan="2"><p>“Virtual Asset Management - Position Management”</p></td><td><p>Position Management Inquiry</p></td><td><p>assets.position_anagement_inquiry_query</p></td></tr>
    <tr><td><p>Position Management Operation</p></td><td><p>assets.position_anagement_inquiry_operation</p></td></tr>
    <tr><td rowspan="3"><p>“Payment Management - Bank Statements - Company Fund Allocation”</p></td><td><p>Company Fund Allocation Inquiry</p></td><td><p>atm.company_fund_allocation_inquiry</p></td></tr>
    <tr><td><p>Company Fund Allocation Operation</p></td><td><p>atm.company_fund_allocation_operation</p></td></tr>
    <tr><td><p>Company Fund Allocation Approval</p></td><td><p>atm.company_fund_allocation_approval</p></td></tr>
    <tr><td rowspan="2"><p>“Business Parameter Settings - Fund Parameters - Settlement Channel Accounts”</p></td><td><p>Settlement Channel Account Inquiry</p></td><td><p>atm.settle_chnl_bank_acct_inquiry</p></td></tr>
    <tr><td><p>Settlement Channel Account Operation</p></td><td><p>atm.settle_chnl_bank_acct_operation</p></td></tr>
    <tr><td rowspan="2"><p>“Business Parameter Settings - Fund Parameters - Fund Allocation Configuration”</p></td><td><p>Fund Allocation Configuration Inquiry</p></td><td><p>atm.funds_alloc_config_inquiry</p></td></tr>
    <tr><td><p>Fund Allocation Configuration Operation</p></td><td><p>atm.funds_alloc_config_operation</p></td></tr>
    </tbody>
    </table>

# Instructions

## <b>Position Inquiry</b>

- Log in to the WBO back-office system and access the corresponding module via “Virtual Asset Management - Position Management.” To perform inquiries, the following permission identifier is required: `assets.position_anagement_inquiry_query`
    - After entering the module, you may filter inquiry criteria based on business needs (such as update time, currency, channel account type, etc.). Enter the relevant parameters and click the “Search” button.
    <img src="/assets/JvHnbj8YfouixXx52kzjrLjlptc.png" src-width="3304" src-height="908" align="center"/>

- If subsequent actions need to be performed in this module, you must additionally apply for the operation permission: `assets.position_anagement_inquiry_operation`
    - By default, the system automatically polls position information every 5 minutes. If you need to query real-time balances for each account and each currency under the current channel, click the [Retrieve Again] button to manually refresh.
        <img src="/assets/VE56bjkijol06yxt9w2jEAl2pof.png" src-width="3274" src-height="882" align="center"/>
    - For high-balance accounts, you may configure a notification position and an interception position based on actual needs:
        - If a notification position has been configured, when the channel available balance is less than the notification position, the system will automatically send alert notifications according to the message subscription settings.
            <img src="/assets/Ly2VbXlProjmRZx6aNlj0T8Ephd.png" src-width="3300" src-height="1316" align="center"/>
        - If an interception position has been configured, when the channel available balance is less than the interception position, the system will send alert notifications according to the message subscription settings. If the account is used for principal interception in withdrawals or fee interception in withdrawals, the system will enforce business interception in the “Virtual Asset Management - Withdrawals - Withdrawal Requests” module, with the rules as follows:
            1. If the withdrawal fee account has insufficient position, the withdrawal request ticket cannot be approved. The system will block it and display: “Insufficient fees for this currency in the channel account. Please perform a fund allocation first.”
            2. If the withdrawal principal account has insufficient position, the withdrawal request ticket cannot be approved. The system will block it and display: “Insufficient principal for this currency in the channel account. Please perform a fund allocation first.”
            3. If both the principal and fee accounts have insufficient position, the withdrawal request ticket cannot be approved. The system will block it and display: “Insufficient principal and fees for this currency in the channel account. Please perform a fund allocation first.”
                <div class="flex gap-3 columns-2" column-size="2">
                <div class="w-[59%]" width-ratio="59">
                                <img src="/assets/FDsPb5B2coHNTNxL6vJjhxGlp4d.png" src-width="3330" src-height="1204" align="center"/>
                                </div>
                <div class="w-[40%]" width-ratio="40">
                                <img src="/assets/RT17bdPgGo98bMxOrZrjJuQAppf.png" src-width="3320" src-height="1752" align="center"/>
                                </div>
                </div>

## Settlement Channel Account Configuration

- Before performing position allocation activities, you must first complete the upstream channel account information configuration. Fund transfer operations between accounts can be performed only after the configuration takes effect.
- Log in to the WBO back-office system and access the corresponding module via “Business Parameter Settings - Fund Parameters - Settlement Channel Accounts.” To perform configuration operations, the following permission identifier is required: `atm.settle_chnl_bank_acct_operation`.
    - After entering the configuration page, you can perform two types of actions: “Create” and “Edit.” The detailed process is as follows:
        - Create account information: Click the “Create” button and accurately complete the settlement channel information (including settlement channel, currency type, and currency) and master account information (including master account number and business scenario). After carefully confirming that all parameters are correct, submit and save; the configuration takes effect immediately.
            <div class="flex gap-3 columns-2" column-size="2">
            <div class="w-[71%]" width-ratio="71">
                        <img src="/assets/DcAUbFQKko1yMMxjjwbjGoHup2b.png" src-width="3266" src-height="702" align="center"/>
                        </div>
            <div class="w-[28%]" width-ratio="28">
                        <img src="/assets/NnAobHohfoUEGIxkDNCjY3i6p3g.png" src-width="3198" src-height="1742" align="center"/>
                        </div>
            </div>
        - Edit account information: Select the account configuration record to be modified and click the “Edit” button. Adjust relevant parameters based on actual business needs and submit to save; the original configuration will be overwritten. Pay close attention to the potential impact of configuration changes on position allocation activities currently in progress and those to be initiated, to avoid business exceptions.
            <img src="/assets/Q0f0bQx1joNLMgxSafWjC9K3pnb.png" src-width="3272" src-height="1738" align="center"/>

- After the configuration is completed, you may use the inquiry permission with permission identifier `atm.settle_chnl_bank_acct_inquiry` to access the corresponding module and query all configured account information. Verify each parameter for accuracy to ensure that the configuration information aligns with actual business requirements.
    <img src="/assets/N68rbPRwtoN33pxWH5Pj8fpypUs.png" src-width="3252" src-height="1744" align="center"/>

## <b>Allocation Rule Configuration</b>

- To ensure that the system can automatically execute fund allocations, you must configure automatic allocation scenarios and the corresponding rules in advance in the back office.
- Log in to the WBO back-office system and access the corresponding module via “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration.” To perform rule configuration operations, the following permission identifier is required: `atm.funds_alloc_config_operation`.
    - After entering the configuration page, you can perform three types of actions: “Create Rule,” “Edit Rule,” and “Copy Rule.” The detailed process is as follows:
        - Create rule: Click the “Create” button, select the allocation type as “Transfer Between Settlement Accounts,” set the debit channel to “settlement_hashkey_hk,” and configure the corresponding automatic transfer rules based on different business scenarios. After confirming that the parameters are correct, submit and save.
            <div class="flex gap-3 columns-2" column-size="2">
            <div class="w-[69%]" width-ratio="69">
                        <img src="/assets/FsIebL48bolN9SxMmrCjJv4jpvf.png" src-width="3320" src-height="1564" align="center"/>
                        </div>
            <div class="w-[30%]" width-ratio="30">
                        <img src="/assets/Flvrbr6xAoxD4oxzshhjvwQxpAb.png" src-width="3248" src-height="3560" align="center"/>
                        </div>
            </div>
        - Edit rule: Select the allocation rule to be modified and click the “Edit” button. Update relevant parameters based on business adjustment needs and submit to save; the existing rule will be overwritten. Pay close attention to the impact of rule changes on automatic allocation activities currently running and subsequent activities to avoid triggering business exceptions.
            <img src="/assets/ACocb5IzQo8C3HxXArPjJG2kpIe.png" src-width="3298" src-height="734" align="center"/>
        - Copy rule: Select an existing configured rule and click the “Copy” button. Modify relevant parameters based on the existing rule to simplify the rule creation process and improve configuration efficiency.
            <img src="/assets/F4MHbgyuko8tufxieWRjwAiDpBh.png" src-width="3298" src-height="734" align="center"/>

- After rule configuration is completed, you may use the inquiry permission with permission identifier `atm.funds_alloc_config_inquiry` to access the corresponding module and query all configured allocation rules. Verify each parameter for accuracy to ensure that the rule configuration meets business requirements for automatic fund allocation.
    <img src="/assets/DaZqbyxfvop6Qpx7ryyjqe1OpJg.png" src-width="3320" src-height="1564" align="center"/>

## <b>Automatic Allocation Operations</b>

- Automatic allocation requires that “Fund Allocation Configuration” be completed in advance (see Section 4.3). Based on the preconfigured trigger conditions, the system will automatically execute allocation operations without manual intervention. Current automatic allocation trigger scenarios fall into the following two categories:
    - Scheduled-task transfers: Supports configuring scheduled tasks (such as daily at midnight) to automatically transfer surplus funds between deposit accounts, trading accounts, etc., according to preset rules. Supported schedule types include calendar day, Hong Kong stock trading day, and week.
    - Event-triggered transfers:
        - When position is insufficient: In “Virtual Asset Management - Position Management,” when the channel available balance for the corresponding master account is less than the interception position, the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration” for that master account. If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the automatic allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.
        - When a withdrawal is submitted (principal): When a withdrawal request is generated in “Virtual Asset Management - Withdrawals - Withdrawal Requests,” the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration” for the principal portion. If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.
        - When a withdrawal is submitted (fee): When a withdrawal request is generated in “Virtual Asset Management - Withdrawals - Withdrawal Requests,” the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration” for the fee portion. If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.
        - When a withdrawal fails (principal): When a withdrawal request fails in “Virtual Asset Management - Withdrawals - Withdrawal Requests,” the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration” for the principal portion. If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.
        - When a withdrawal fails (fee): When a withdrawal request fails in “Virtual Asset Management - Withdrawals - Withdrawal Requests,” the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration” for the fee portion. If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.
        - When a deposit succeeds: When a deposit is shown as successful in “Virtual Asset Management - Deposits - Deposit Records,” the system will match “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration.” If there is an enabled rule (allocation strategy = automatic, status = enabled, and highest priority), the system will initiate an allocation automatically according to the rule. If the allocation fails due to insufficient balance in the debit account, you must initiate a manual transfer afterward.

- Operators can use the “Payment Management - Bank Statements - Company Fund Allocation” module (requires the `atm.company_fund_allocation_inquiry` inquiry permission) to view execution records for automatic allocations, including key information such as allocation time, amount, currency, initiating account, receiving account, and business reference number, for traceability and verification.
    <img src="/assets/SQE8bIDDaol8f7xxalijPBKhpfc.png" src-width="3294" src-height="670" align="center"/>

- If an automatic allocation fails, the system will clearly display the reason for failure (such as insufficient account balance). Operators must promptly investigate and resolve the issue. After adjusting the relevant rules or adding funds, a manual retry may be triggered (requires the corresponding operation permission for “Payment Management - Bank Statements - Company Fund Allocation”) to ensure successful completion of the fund allocation.
    <img src="/assets/Q9HEb3JVIoSKMsx3A88jmqIPpTf.png" src-width="3304" src-height="852" align="center"/>

## <b>Manual Allocation Operations</b>

- Log in to the WBO back-office system and access the corresponding module via “Payment Management - Bank Statements - Company Fund Allocation.” To perform manual allocation operations, the following permission identifier is required: `atm.company_fund_allocation_operation`.
    - Click the “Create” button and accurately complete the allocation information, including initiating account, receiving account, allocation currency, allocation amount, and allocation remarks (the reason for allocation must be clearly stated for subsequent traceability and verification). After carefully confirming that all information is correct, submit it.
        <div class="flex gap-3 columns-2" column-size="2">
        <div class="w-[84%]" width-ratio="84">
                <img src="/assets/JqFVbDNxmoevCmxGIdAjsFgVphb.png" src-width="3296" src-height="694" align="center"/>
                </div>
        <div class="w-[15%]" width-ratio="15">
                <img src="/assets/VrEebTP1fo3AtQxXRq9jB6RBp1g.png" src-width="2856" src-height="3348" align="center"/>
                </div>
        </div>

- Allocation requests submitted manually via the “Create” button, or allocation requests whose approval strategy is “Ticket Approval” in “Business Parameter Settings - Fund Parameters - Fund Allocation Configuration,” will automatically enter the approval workflow. The request must be reviewed by an approver with permission identifier `atm.company_fund_allocation_approval`:
    - After approval, the system will automatically execute the allocation operation.
    - If the approval is rejected, the allocation request will fail. If the corresponding fund allocation is still required, you must resubmit a manual allocation request.
    <div class="flex gap-3 columns-2" column-size="2">
    <div class="w-[76%]" width-ratio="76">
        <img src="/assets/Lj1tbnlHwobHV9xWVRZjw80qpcc.png" src-width="3286" src-height="686" align="center"/>
        </div>
    <div class="w-[23%]" width-ratio="23">
        <img src="/assets/LYS6b3NN8oCOTlxo1TYj6zf2pPR.png" src-width="2514" src-height="1758" align="center"/>
        </div>
    </div>

- After the allocation operation is completed, operators may use the inquiry permission with permission identifier `atm.company_fund_allocation_inquiry` to view the execution status and record details of manual allocations, verifying the relevant data item by item to ensure the allocation process is compliant and the data is accurate.
    <img src="/assets/UVc7b9jqSo884XxDcoIjZQzLpJd.png" src-width="3284" src-height="1166" align="center"/>

# <b>Important Notes</b>

- Operators must properly safeguard account passwords and must not lend their accounts to others. After logging in, lock the system in a timely manner, and log out properly when exiting to prevent account theft and resulting fund risks.
- All operations must be performed strictly in accordance with this manual. Unauthorized operations and non-compliant allocations are strictly prohibited. During operations, carefully verify relevant parameters (such as account information, amount, and currency) to avoid errors.
- For key operations such as allocation rule configuration and manual allocations, records must be properly retained for subsequent audit and verification. If any abnormal situations are identified (such as position anomalies, allocation failures, or data discrepancies), report them to the administrator promptly and do not conceal them.
- System permission changes must be performed centrally by administrators. If operators need permission adjustments, they must submit a formal request, which takes effect only after approval. After permissions are changed, operators must promptly familiarize themselves with the operational scope corresponding to the new permissions.
- Fiat and cryptocurrency position changes are sensitive. Operators must monitor position status in real time, especially position balances near automatic allocation trigger thresholds, and prepare funds in advance to avoid disruptions to normal business operations due to insufficient position.
```

