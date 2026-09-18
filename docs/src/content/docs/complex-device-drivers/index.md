---
title: Complex Device Drivers
description: Modules of the Complex Device Drivers layer.
---

This section documents the **Complex Device Drivers (CDD)** layer.

## Analog Acquisition and Timers

| Module | Repository directories | Origin |
|---|---|---|
| [Analog to Digital Converter 0 Configuration And Use (CM300A_ADC0CfgAndUse)](./CM300A_ADC0CfgAndUse/) | `CM300A_ADC0CfgAndUse_Design` | In-house (custom) |
| [Adc0 Configuration And Use (CM300A_Adc0CfgAndUse)](./CM300A_Adc0CfgAndUse/) | `CM300A_Adc0CfgAndUse_Impl` | In-house (custom) |
| [Adc1 Configuration And Use (CM320A_Adc1CfgAndUse)](./CM320A_Adc1CfgAndUse/) | `CM320A_Adc1CfgAndUse_Design`, `CM320A_Adc1CfgAndUse_Impl` | In-house (custom) |
| [Analog to Digital Converter Diagnostics (CM340A_AdcDiagc)](./CM340A_AdcDiagc/) | `CM340A_AdcDiagc_Design`, `CM340A_AdcDiagc_Impl` | In-house (custom) |
| [Sensor Measurement Start (CM410A_SnsrMeasStrt)](./CM410A_SnsrMeasStrt/) | `CM410A_SnsrMeasStrt_Design`, `CM410A_SnsrMeasStrt_Impl` | In-house (custom) |
| [Tauj0 Configuration And Use (CM455A_Tauj0CfgAndUse)](./CM455A_Tauj0CfgAndUse/) | `CM455A_Tauj0CfgAndUse_Design`, `CM455A_Tauj0CfgAndUse_Impl` | In-house (custom) |
| [Tauj1 Configuration And Use (CM460A_Tauj1CfgAndUse)](./CM460A_Tauj1CfgAndUse/) | `CM460A_Tauj1CfgAndUse_Design`, `CM460A_Tauj1CfgAndUse_Impl` | In-house (custom) |
| [Timer Synchronous Generator 31 Configuration And Use (CM475A_TSG31CfgAndUse)](./CM475A_TSG31CfgAndUse/) | `CM475A_TSG31CfgAndUse_Design`, `CM475A_TSG31CfgAndUse_Impl` | In-house (custom) |

## Direct Memory Access

| Module | Repository directories | Origin |
|---|---|---|
| [Direct Memory Access Configuration And Use (CM200A_DmaCfgAndUse)](./CM200A_DmaCfgAndUse/) | `CM200A_DmaCfgAndUse_Design`, `CM200A_DmaCfgAndUse_Impl` | In-house (custom) |

## Measurement and Arbitration

| Module | Repository directories | Origin |
|---|---|---|
| [Current Measurement (ES200A_CurrMeas)](./ES200A_CurrMeas/) | `ES200A_CurrMeas_Design`, `ES200A_CurrMeas_Impl` | In-house (custom) |
| [Current Measurement Arbitration (ES208A_CurrMeasArbn)](./ES208A_CurrMeasArbn/) | `ES208A_CurrMeasArbn_Design`, `ES208A_CurrMeasArbn_Impl` | In-house (custom) |
| [Current Measurement Correlation (ES209A_CurrMeasCorrln)](./ES209A_CurrMeasCorrln/) | `ES209A_CurrMeasCorrln_Design`, `ES209A_CurrMeasCorrln_Impl` | In-house (custom) |
| [Control Unit Temperature Measurement (ES210A_EcuTMeas)](./ES210A_EcuTMeas/) | `ES210A_EcuTMeas_Design`, `ES210A_EcuTMeas_Impl` | In-house (custom) |
| [Handwheel Torque Arbitration (ES228A_HwTqArbn)](./ES228A_HwTqArbn/) | `ES228A_HwTqArbn_Design`, `ES228A_HwTqArbn_Impl` | In-house (custom) |
| [Handwheel Torque Correlation (ES229A_HwTqCorrln)](./ES229A_HwTqCorrln/) | `ES229A_HwTqCorrln_Design`, `ES229A_HwTqCorrln_Impl` | In-house (custom) |
| [Handwheel Angle Arbitration (ES238A_HwAgArbn)](./ES238A_HwAgArbn/) | `ES238A_HwAgArbn_Design`, `ES238A_HwAgArbn_Impl` | In-house (custom) |
| [Handwheel Angle Correlation (ES239A_HwAgCorrln)](./ES239A_HwAgCorrln/) | `ES239A_HwAgCorrln_Design`, `ES239A_HwAgCorrln_Impl` | In-house (custom) |
| [Motor Angle 2 Measurement (ES241A_MotAg2Meas)](./ES241A_MotAg2Meas/) | `ES241A_MotAg2Meas_Design`, `ES241A_MotAg2Meas_Impl` | In-house (custom) |
| [Motor Angle Comparison (ES247A_MotAgCmp)](./ES247A_MotAgCmp/) | `ES247A_MotAgCmp_Design`, `ES247A_MotAgCmp_Impl` | In-house (custom) |
| [Motor Angle Arbitration (ES248A_MotAgArbn)](./ES248A_MotAgArbn/) | `ES248A_MotAgArbn_Design`, `ES248A_MotAgArbn_Impl` | In-house (custom) |
| [Motor Angle Correlation (ES249A_MotAgCorrln)](./ES249A_MotAgCorrln/) | `ES249A_MotAgCorrln_Design`, `ES249A_MotAgCorrln_Impl` | In-house (custom) |
| [Battery Voltage (ES250A_BattVltg)](./ES250A_BattVltg/) | `ES250A_BattVltg_Design`, `ES250A_BattVltg_Impl` | In-house (custom) |
| [Battery Voltage Correlation (ES259A_BattVltgCorrln)](./ES259A_BattVltgCorrln/) | `ES259A_BattVltgCorrln_Design`, `ES259A_BattVltgCorrln_Impl` | In-house (custom) |

## Motor Control Management

| Module | Repository directories | Origin |
|---|---|---|
| [Motor Control Manager (AR300A_MotCtrlMgr)](./AR300A_MotCtrlMgr/) | `AR300A_MotCtrlMgr_Design`, `AR300A_MotCtrlMgr_Impl` | In-house (custom) |

## Motor Drive and Voltage Generation

| Module | Repository directories | Origin |
|---|---|---|
| [Sine Voltage Generation (ES300A_SinVltgGenn)](./ES300A_SinVltgGenn/) | `ES300A_SinVltgGenn_Design`, `ES300A_SinVltgGenn_Impl` | In-house (custom) |
| [Gate Drv0 Control (ES311A_GateDrv0Ctrl)](./ES311A_GateDrv0Ctrl/) | `ES311A_GateDrv0Ctrl_Design`, `ES311A_GateDrv0Ctrl_Impl` | In-house (custom) |
| [Gate Drv1 Control (ES312A_GateDrv1Ctrl)](./ES312A_GateDrv1Ctrl/) | `ES312A_GateDrv1Ctrl_Design`, `ES312A_GateDrv1Ctrl_Impl` | In-house (custom) |
| [Motor Drive Diagnostics (ES320A_MotDrvDiagc)](./ES320A_MotDrvDiagc/) | `ES320A_MotDrvDiagc_Design`, `ES320A_MotDrvDiagc_Impl` | In-house (custom) |

## Power, Thermal and System State

| Module | Repository directories | Origin |
|---|---|---|
| [Microcontroller Diagnostics (ES002A_McuDiagc)](./ES002A_McuDiagc/) | `ES002A_McuDiagc_Design`, `ES002A_McuDiagc_Impl` | In-house (custom) |
| [Power Disconnect (ES003A_PwrDiscnct)](./ES003A_PwrDiscnct/) | `ES003A_PwrDiscnct_Design`, `ES003A_PwrDiscnct_Impl` | In-house (custom) |
| [Power-Up Sequence (ES004A_PwrUpSeq)](./ES004A_PwrUpSeq/) | `ES004A_PwrUpSeq_Design`, `ES004A_PwrUpSeq_Impl` | In-house (custom) |
| [Temperature Monitor (ES005A_TmplMonr)](./ES005A_TmplMonr/) | `ES005A_TmplMonr_Design`, `ES005A_TmplMonr_Impl` | In-house (custom) |
| [Non-Volatile Memory (ES006A_NvM)](./ES006A_NvM/) | `ES006A_NvM_Design`, `ES006A_NvM_Impl` | In-house (custom) |
| [Power Supply (ES008A_PwrSply)](./ES008A_PwrSply/) | `ES008A_PwrSply_Design`, `ES008A_PwrSply_Impl` | In-house (custom) |
| [System State Mode (ES100A_SysStMod)](./ES100A_SysStMod/) | `ES100A_SysStMod_Design`, `ES100A_SysStMod_Impl` | In-house (custom) |
| [Diagnostics Manager (ES101A_DiagcMgr)](./ES101A_DiagcMgr/) | `ES101A_DiagcMgr_Design`, `ES101A_DiagcMgr_Impl` | In-house (custom) |
| [Polarity Configuration (ES102A_PolarityCfg)](./ES102A_PolarityCfg/) | `ES102A_PolarityCfg_Design`, `ES102A_PolarityCfg_Impl` | In-house (custom) |
| [Calibration Protocol Interface (ES104A_XcpIf)](./ES104A_XcpIf/) | `ES104A_XcpIf_Impl` | In-house (custom) |
| [Steering Health Signal Normalization (ES105A_StHlthSigNormn)](./ES105A_StHlthSigNormn/) | `ES105A_StHlthSigNormn_Design`, `ES105A_StHlthSigNormn_Impl` | In-house (custom) |
| [Steering Health Signal Static (ES106A_StHlthSigStc)](./ES106A_StHlthSigStc/) | `ES106A_StHlthSigStc_Design`, `ES106A_StHlthSigStc_Impl` | In-house (custom) |

## Serial Interfaces and Position Sensing

| Module | Repository directories | Origin |
|---|---|---|
| [Clocked Serial Interface G 0 Configuration And Use (CM600A_CSIG0CfgAndUse)](./CM600A_CSIG0CfgAndUse/) | `CM600A_CSIG0CfgAndUse_Design` | In-house (custom) |
| [Clocked Serial Interface H 0 Configuration And Use (CM610A_CSIH0CfgAndUse)](./CM610A_CSIH0CfgAndUse/) | `CM610A_CSIH0CfgAndUse_Design` | In-house (custom) |
| [Motor Ag0 Measurement (CM620A_MotAg0Meas)](./CM620A_MotAg0Meas/) | `CM620A_MotAg0Meas_Design`, `CM620A_MotAg0Meas_Impl` | In-house (custom) |
| [Clocked Serial Interface H 2 Configuration And Use (CM630A_CSIH2CfgAndUse)](./CM630A_CSIH2CfgAndUse/) | `CM630A_CSIH2CfgAndUse_Design` | In-house (custom) |
| [Motor Ag1 Measurement (CM640A_MotAg1Meas)](./CM640A_MotAg1Meas/) | `CM640A_MotAg1Meas_Design`, `CM640A_MotAg1Meas_Impl` | In-house (custom) |
| [Handwheel Tq0 Measurement (CM650A_HwTq0Meas)](./CM650A_HwTq0Meas/) | `CM650A_HwTq0Meas_Design`, `CM650A_HwTq0Meas_Impl` | In-house (custom) |
| [Handwheel Tq1 Measurement (CM660A_HwTq1Meas)](./CM660A_HwTq1Meas/) | `CM660A_HwTq1Meas_Design`, `CM660A_HwTq1Meas_Impl` | In-house (custom) |
| [Handwheel Ag1 Measurement (CM670A_HwAg1Meas)](./CM670A_HwAg1Meas/) | `CM670A_HwAg1Meas_Design`, `CM670A_HwAg1Meas_Impl` | In-house (custom) |
| [Handwheel Tq2 Measurement (CM680A_HwTq2Meas)](./CM680A_HwTq2Meas/) | `CM680A_HwTq2Meas_Design`, `CM680A_HwTq2Meas_Impl` | In-house (custom) |
| [Handwheel Ag0 Measurement (CM690A_HwAg0Meas)](./CM690A_HwAg0Meas/) | `CM690A_HwAg0Meas_Design`, `CM690A_HwAg0Meas_Impl` | In-house (custom) |
| [Handwheel Tq3 Measurement (CM700A_HwTq3Meas)](./CM700A_HwTq3Meas/) | `CM700A_HwTq3Meas_Design`, `CM700A_HwTq3Meas_Impl` | In-house (custom) |

## Synchronisation and Cyclic Redundancy Check

| Module | Repository directories | Origin |
|---|---|---|
| [Synchronous Cyclic Redundancy Check (CM800A_SyncCrc)](./CM800A_SyncCrc/) | `CM800A_SyncCrc_Design`, `CM800A_SyncCrc_Impl` | In-house (custom) |

## System, Memory and Startup

| Module | Repository directories | Origin |
|---|---|---|
| [Startup Sequence (CM100A_StrtUpSeq)](./CM100A_StrtUpSeq/) | `CM100A_StrtUpSeq_Design` | In-house (custom) |
| [Exception Handling (CM101A_ExcpnHndlg)](./CM101A_ExcpnHndlg/) | `CM101A_ExcpnHndlg_Design`, `CM101A_ExcpnHndlg_Impl` | In-house (custom) |
| [Flash Memory (CM102A_FlsMem)](./CM102A_FlsMem/) | `CM102A_FlsMem_Design`, `CM102A_FlsMem_Impl` | In-house (custom) |
| [Random Access Memory Memory (CM103A_RamMem)](./CM103A_RamMem/) | `CM103A_RamMem_Design`, `CM103A_RamMem_Impl` | In-house (custom) |
| [Engine Control Module Output And Diagnostics (CM104A_EcmOutpAndDiagc)](./CM104A_EcmOutpAndDiagc/) | `CM104A_EcmOutpAndDiagc_Design`, `CM104A_EcmOutpAndDiagc_Impl` | In-house (custom) |
| [Microcontroller Unit Core Configuration And Diagnostics (CM106A_McuCoreCfgAndDiagc)](./CM106A_McuCoreCfgAndDiagc/) | `CM106A_McuCoreCfgAndDiagc_Design`, `CM106A_McuCoreCfgAndDiagc_Impl` | In-house (custom) |
| [Guard Configuration And Diagnostics (CM107A_GuardCfgAndDiagc)](./CM107A_GuardCfgAndDiagc/) | `CM107A_GuardCfgAndDiagc_Design`, `CM107A_GuardCfgAndDiagc_Impl` | In-house (custom) |
| [Data And Address Parity (CM108A_DataAndAdrPar)](./CM108A_DataAndAdrPar/) | `CM108A_DataAndAdrPar_Design`, `CM108A_DataAndAdrPar_Impl` | In-house (custom) |
| [Clock Configuration And Mon (CM109A_ClkCfgAndMon)](./CM109A_ClkCfgAndMon/) | `CM109A_ClkCfgAndMon_Design`, `CM109A_ClkCfgAndMon_Impl` | In-house (custom) |
| [Verify Critical Registers (CM111A_VrfyCritReg)](./CM111A_VrfyCritReg/) | `CM111A_VrfyCritReg_Design`, `CM111A_VrfyCritReg_Impl` | In-house (custom) |

## Tuning and Global Parameters

| Module | Repository directories | Origin |
|---|---|---|
| [Tuning Selection Management (ES400A_TunSelnMngt)](./ES400A_TunSelnMngt/) | `ES400A_TunSelnMngt_Design`, `ES400A_TunSelnMngt_Impl` | In-house (custom) |

Back to the [documentation home](/).
