---
title: 2026-04-08 Release Notes
slug: RZYZwbpBCia6TYkzJBNcgsqcnCh
sidebar_position: 0
---


# 2026-04-08 Release Notes

# 🪀 Optimization and Bugfix

- eDDA Multi-Currency Expansion (Added CNH Support)
    - eDDA originally only supported HKD authorization and deposit. This upgrade adds CNH currency configuration.After CNH configuration is completed in the backend, customers can use HKD / CNH for authorization and deposit simultaneously.
    - Path: Cash Management - Deposit/Withdrawal Methods - eDDA
    <img src="/assets/GnCrbcgwQoluDwxyLk2jhVLQp4c.png" src-width="3304" src-height="1128" align="center"/>

- Added API raw data and interaction optimization for bank statements
    - Integrated the original menu entries "Deposit Bill Settings" and "Auto Tagging Rules" into the "Bill Rules" menu in the form of tabs.
    - Path: WBO - Cash Management - Bank Statement - Bill Rules
    - For banks connected via API channels, the complete bill data and deposit messages synchronously obtained by the system can be queried in the backend. Manual triggering is supported to re-push API bills that were not automatically pushed by the system. The automatic crediting status of deposit messages can also be viewed in the backend for manual verification and intervention.
    - Path: WBO - Cash Management - Bank Statement - API Raw Data
    - Permission：
        - API Deposit Message Inquiry atm.api_deposit_message_inquiry
        - API Billing Inquiry atm.api_billing_inquiry
        - API Billing Audit atm.api_billing_audit
        - API Billing Operation atm.api_billing_operation
    <img src="/assets/BepJb0Ip5ovoHxxOLATj5umLp7d.png" src-width="3806" src-height="858" align="center"/>
    <img src="/assets/MPkbbXy7IokJL5xGs73jhPlopzf.png" src-width="3810" src-height="928" align="center"/>
    <img src="/assets/FCUUbx46EonM2kxt6zKj6D8Gptf.png" src-width="3320" src-height="1106" align="center"/>
    
