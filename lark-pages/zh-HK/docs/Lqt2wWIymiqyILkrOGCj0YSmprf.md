---
title: 2026-04-08 更新日誌
slug: M2skwc1hdiazLEkdSDgjXtCwpFe
sidebar_position: 0
version: stable
---


# 2026-04-08 更新日誌

# 🪀 改進與修復

- eDDA 多幣種擴展（新增 CNH 支援）
    - eDDA 原有僅支援 HKD 授權與入金，本次升級新增 CNH 幣種配置後台完成 CNH 配置後，客戶可同時使用 HKD / CNH 進行授權及入金
    - 路徑：款項管理 - 出入金方式 - eDDA
    <img src="/assets/WkENbBL7oofdE6xy3qWjEoK1pfd.png" src-width="3272" src-height="1162" align="center"/>

- 銀行帳單新增 API 原始資料以及互動優化
    - 將原選單入口「入金帳單設定」與「自動標記規則」以分頁（Tab）形式整合至「帳單規則」選單下
    - 路徑：WBO - 款項管理 - 銀行帳單 - 帳單規則
    - 針對透過 API 通道對接的銀行，系統同步取得之完整帳單資料及入金訊息可於後台查詢；支援手動觸發重新推送系統未自動推送之 API 帳單，同時可於後台檢視入金訊息之自動入帳狀態，利於人工核對與介入處理。
    - 路徑：WBO - 款項管理 - 銀行帳單 - API 原始數據
    - 權限
        - API 入金消息查詢 atm.api_deposit_message_inquiry
        - API 賬單查詢 atm.api_billing_inquiry
        - API 賬單審核 atm.api_billing_audit
        - API 賬單操作 atm.api_billing_operation
    <img src="/assets/KFzpbnVoBouyU7x451zjwkWqpuy.png" src-width="3808" src-height="822" align="center"/>
    <img src="/assets/HCvvbaHmVoRmjHxOA7cjTVvTpjf.png" src-width="3822" src-height="1154" align="center"/>
    <img src="/assets/FztnbnrXvo6zJVxJTEGjrqcDpPh.png" src-width="3288" src-height="1128" align="center"/>

