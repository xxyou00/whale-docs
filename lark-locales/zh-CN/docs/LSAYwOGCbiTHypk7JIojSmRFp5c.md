---
title: 2026-01-26 更新日志
slug: LSAYwOGCbiTHypk7JIojSmRFp5c
sidebar_position: 0
version: stable
---


# 2026-03-16 更新日志

# 🎉 新功能

- 头寸查询与即时获取 / 提示头寸与拦截头寸配置 / 结算渠道帐户配置 / 资金调拨规则配置（新建 / 编辑 / 复制） / 定时任务自动调拨 / 事件触发自动调拨（头寸不足、出金提交 / 失败、入金成功） / 手动资金调拨与工单审批 / 调拨记录查询与状态核对
    - 新增头寸查询、即时余额重新获取功能，支援按渠道、币种、帐号类型筛选查询，同时适用于法币与加密货币。
    - 新增提示头寸、拦截头寸配置及对应告警机制，出金场景支援本金与手续费不足拦截。
        - 路径：虚拟资产管理 - 头寸管理
    - 新增结算渠道帐户配置功能，用于头寸调拨前的上游帐户资讯维护。
        - 路径：业务参数设置 - 资金参数 - 结算渠道帐户
    - 新增资金调拨规则配置，支援结算帐户间划转规则的新建、编辑与复制。
    - 实现自动调拨能力，支援定时任务划转与多场景事件触发划转。
        - 路径：业务参数设置 - 资金参数 - 资金调拨配置
    - 上线手动调拨与审批流程，支援发起、审核、驳回、重新申请。
    - 优化调拨记录查询功能，操作人员可查询调拨状态、金额、币种、发起 / 接收帐户、业务单号等详细资讯，确保流程可追溯、数据准确无误。
        - 路径：款项管理 - 银行帐单 - 公司资金调拨
    - 权限：
        - 头寸管理查询 assets.position_anagement_inquiry_query
        - 头寸管理操作 assets.position_anagement_inquiry_operation
        - 公司资金调拨查询 atm.company_fund_allocation_inquiry
        - 公司资金调拨操作 atm.company_fund_allocation_operation
        - 公司资金调拨审批 atm.company_fund_allocation_approval
        - 结算渠道帐户查询 atm.settle_chnl_bank_acct_inquiry
        - 结算渠道帐户操作 atm.settle_chnl_bank_acct_operation
        - 资金调拨配置查询 atm.funds_alloc_config_inquiry
        - 资金调拨配置操作 atm.funds_alloc_config_operation
    <img src="/assets/SkUmbZcE2oacZXxGIz6j2cCGpad.png" src-width="3814" src-height="1038" align="center"/>
    <img src="/assets/XAHub0cj7os9b6xb80vjslx7pMg.png" src-width="3800" src-height="1632" align="center"/>
    <img src="/assets/MrIQb8eUuoV9vTxVlcajuePqpVf.png" src-width="3794" src-height="1546" align="center"/>
    <img src="/assets/KguWbgtUTot5WkxltdZjw7rxptc.png" src-width="3816" src-height="1196" align="center"/>

