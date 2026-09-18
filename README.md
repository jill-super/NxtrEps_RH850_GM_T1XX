# Electric Power Steering System for the General Motors T1XX Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Language: C](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Standard: AUTOSAR](https://img.shields.io/badge/Standard-AUTOSAR-green.svg)](https://www.autosar.org/)
[![Safety: ISO 26262 ASIL D](https://img.shields.io/badge/Safety-ISO_26262_ASIL_D-red.svg)](https://www.iso.org/standard/68383.html)

Complete **Electric Power Steering** system software for the **General Motors T1XX** vehicle platform, running on a **Renesas RH850** microcontroller and structured according to the **AUTOSAR (AUTomotive Open System ARchitecture)** layered model.

> **Naming convention:** this file and the whole documentation use expanded **long names** for readability. The short repository name is always kept in parentheses, e.g. Assist (`SF001A_Assi`). See the [glossary](docs/src/content/docs/overview/glossary.md).

## Table of Contents

- [Features](#features)
- [Repository Structure](#repository-structure)
- [AUTOSAR Layers and Modules](#autosar-layers-and-modules)
- [Vector-Provided Code versus In-House Code](#vector-provided-code-versus-in-house-code)
- [Documentation Site](#documentation-site)
- [Installation and Build](#installation-and-build)
- [General Motors T1XX Platform](#general-motors-t1xx-platform)
- [Contributing](#contributing)
- [License](#license)

## Features

<details>
<summary><strong>Key components (click to expand)</strong></summary>

- **Renesas RH850**: the microcontroller unit executing the steering control.
- **AUTOSAR**: the software architecture standard for automotive embedded systems.
- **ISO 26262 ASIL D (Automotive Safety Integrity Level D)**: the functional-safety target for the system.
- **Controller Area Network**: the in-vehicle communication protocol.
- **Unified Diagnostic Services**: the on-board diagnostics protocol.
- **Universal Measurement and Calibration Protocol**: measurement and calibration access.

</details>

<details>
<summary><strong>Functionality (click to expand)</strong></summary>

- Precise power-assisted steering control (assist, return, damping and compensation functions).
- Electric-motor power management, current regulation and thermal protection.
- Redundant sensing with arbitration and correlation (handwheel torque, handwheel angle, motor angle, current, voltage).
- Diagnostics, fault injection support and manufacturing services.
- Integration of communication security (cybersecurity).

</details>

## Repository Structure

```text
.
├── docs/                                   # Documentation site source (Astro + Starlight project root)
│   ├── astro.config.mjs                    # Site config; Pages URL auto-detected, nothing hardcoded
│   ├── package.json
│   └── src/content/docs/                   # One folder per AUTOSAR layer, one page per module
├── SF*/ CF*/ MM*/ DF*/ NM*/ GM_00*/        # Application Software components (design + implementation pairs)
├── CM*/ ES*/ AR300*/                       # Complex Device Drivers (design + implementation pairs)
├── BswM/ Dem/ Det/ EcuM/ NvM/ WdgM/ Xcp/   # Basic Software Services (Vector-provided)
├── IoHwAb/ Fee/ MemIf/ WdgIf/              # Electronic Control Unit Abstraction
├── Mcu/ Port/ Dio/ Spi/ Fls/ Wdg/ Can/     # Microcontroller Abstraction Layer drivers
├── Il/ Tp/ Nm/ Diag/                       # Communication stack
├── Os/ Rte/                                # Operating System and Runtime Environment
├── AR1*/ Crc/ *GlbPrm*/                    # Shared libraries and global parameters
├── TL*/ AR20*/ VectorBswSuprt/             # Host-side tools and support packages
├── EcuC/ CM010*/ GM_T1XX_EPS_RH850/        # System integration
├── LICENSE                               # MIT License
└── README.md                             # This file
```

Each logical module usually spans two directories: a `*_Design` package (functional and design documents) and a `*_Impl` package (source code, AUTOSAR model, configuration, integration scripts).

## AUTOSAR Layers and Modules

The repository holds **221 logical modules**: **187** in-house (custom), **29** Vector-provided, **3** Vector-provided but customised, and **2** from other origins. The full per-module documentation, including converted reference documents, lives in the [documentation site](docs/).

<details>
<summary><strong>Application Software — 100 modules</strong> (Application Software (ASW))</summary>

Steering functions, customer functions, serial-communication proxies, diagnostics and manufacturing services, implemented as AUTOSAR software components.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| General Motors Overall State Manager | `CF009A_GmOvrlStMgr` | In-house (custom) |
| General Motors Torque Arbitration | `CF010A_GmTqArbn` | In-house (custom) |
| General Motors Start Stop | `CF012A_GmStrtStop` | In-house (custom) |
| General Motors Vehicle Speed Arbitration | `CF016A_GMVehSpdArbn` | In-house (custom) |
| General Motors Vehicle Speed Arbitration | `CF016A_GmVehSpdArbn` | In-house (custom) |
| General Motors Vehicle Power Mode | `CF017A_GMVehPwrMod` | In-house (custom) |
| General Motors Vehicle Power Mode | `CF017A_GmVehPwrMod` | In-house (custom) |
| General Motors Road Wheel Input Qualifier | `CF018A_GmRoadWhlInQlfr` | In-house (custom) |
| General Motors Function Diagnostic Arbitration | `CF025A_GmFctDiArbn` | In-house (custom) |
| Fault Injection | `DF001A_FltInj` | In-house (custom) |
| Sweep | `DF002A_Swp` | In-house (custom) |
| Microcontroller Error Injection | `DF003A_McuErrInj` | In-house (custom) |
| General Motors 000 A General Motors Local Area Network 3 1 Machine RH 850 | `GM_000A_GMLAN3.1MchRH850` | In-house (custom) |
| General Motors 001 A Checkpoint | `GM_001A_ChkPt` | In-house (custom) |
| General Motors 002 A Part Number | `GM_002A_PartNr` | In-house (custom) |
| General Motors 003 A Customer Diagnostics | `GM_003A_CustDiagc` | In-house (custom) |
| Serial Communication Input Proxy | `MM000A_SerlComInpProxy` | In-house (custom) |
| General Motors Msg0 C5 Bus High Speed | `MM001A_GmMsg0C5BusHiSpd` | In-house (custom) |
| General Motors Msg0 C9 Bus High Speed | `MM002A_GmMsg0C9BusHiSpd` | In-house (custom) |
| General Motors Msg17 D Bus High Speed | `MM004A_GmMsg17DBusHiSpd` | In-house (custom) |
| General Motors Msg180 Bus High Speed | `MM005A_GmMsg180BusHiSpd` | In-house (custom) |
| General Motors Msg1 E9 Bus High Speed | `MM006A_GmMsg1E9BusHiSpd` | In-house (custom) |
| General Motors Msg1 F1 Bus High Speed | `MM007A_GmMsg1F1BusHiSpd` | In-house (custom) |
| General Motors Msg1 F5 Bus High Speed | `MM008A_GmMsg1F5BusHiSpd` | In-house (custom) |
| General Motors Msg214 Bus High Speed | `MM009A_GmMsg214BusHiSpd` | In-house (custom) |
| General Motors Msg232 Bus High Speed | `MM010A_GmMsg232BusHiSpd` | In-house (custom) |
| General Motors Msg348 Bus High Speed | `MM011A_GmMsg348BusHiSpd` | In-house (custom) |
| General Motors Msg34 A Bus High Speed | `MM012A_GmMsg34ABusHiSpd` | In-house (custom) |
| General Motors Msg3 F1 Bus High Speed | `MM014A_GmMsg3F1BusHiSpd` | In-house (custom) |
| General Motors Msg500 Bus High Speed | `MM016A_GmMsg500BusHiSpd` | In-house (custom) |
| General Motors Msg180 Bus Chassis Expansion | `MM017A_GmMsg180BusChassisExp` | In-house (custom) |
| General Motors Msg182 Bus Chassis Expansion | `MM018A_GmMsg182BusChassisExp` | In-house (custom) |
| General Motors Msg337 Bus Chassis Expansion | `MM019A_GmMsg337BusChassisExp` | In-house (custom) |
| General Motors Msg348 Bus Chassis Expansion | `MM020A_GmMsg348BusChassisExp` | In-house (custom) |
| General Motors Msg34 A Bus Chassis Expansion | `MM021A_GmMsg34ABusChassisExp` | In-house (custom) |
| General Motors Msg4 D1 Bus High Speed | `MM022A_GmMsg4D1BusHiSpd` | In-house (custom) |
| Serial Communication Output Proxy | `MM500A_SerlComOutpProxy` | In-house (custom) |
| General Motors Msg148 Bus High Speed | `MM501A_GmMsg148BusHiSpd` | In-house (custom) |
| General Motors Msg184 Bus High Speed | `MM502A_GmMsg184BusHiSpd` | In-house (custom) |
| General Motors Msg1 E5 Bus High Speed | `MM503A_GmMsg1E5BusHiSpd` | In-house (custom) |
| General Motors Msg778 Bus High Speed | `MM504A_GmMsg778BusHiSpd` | In-house (custom) |
| General Motors Msg1 CA Bus Chassis Expansion | `MM505A_GmMsg1CABusChassisExp` | In-house (custom) |
| General Motors Msg1 E5 Bus Chassis Expansion | `MM506A_GmMsg1E5BusChassisExp` | In-house (custom) |
| General Motors Msg335 Bus Chassis Expansion | `MM507A_GmMsg335BusChassisExp` | In-house (custom) |
| Common Manufacturing Services | `NM001A_CmnMfgSrv` | In-house (custom) |
| Common Manufacturing Services Interface | `NM002A_CmnMfgSrvIf` | In-house (custom) |
| Nexteer Software Identifiers | `NM003A_NxtrSwIds` | In-house (custom) |
| Nexteer Calibration Identifiers | `NM004A_NxtrCalIds` | In-house (custom) |
| Programming Manufacturing Services | `NM010A_ProgMfgSrv` | In-house (custom) |
| Motor Velocity Control | `NM100A_MotVelCtrl` | In-house (custom) |
| Assist | `SF001A_Assi` | In-house (custom) |
| Return | `SF002A_Rtn` | In-house (custom) |
| Damping | `SF003A_Dampg` | In-house (custom) |
| Assist Summation Limiter | `SF004B_AssiSumLim` | In-house (custom) |
| Steering Output Control | `SF005A_StOutpCtrl` | In-house (custom) |
| Torque Estimation | `SF006A_TEstimn` | In-house (custom) |
| System Friction Learning | `SF007A_SysFricLrng` | In-house (custom) |
| Duty Cycle Thermal Protection | `SF009A_DutyCycThermProtn` | In-house (custom) |
| End of Travel Learning | `SF011A_EotLrng` | In-house (custom) |
| Hysteresis Compensation | `SF012A_HysCmp` | In-house (custom) |
| Pull Compensation Active | `SF013A_PullCmpActv` | In-house (custom) |
| Inertia Compensation Velocity | `SF014A_InertiaCmpVel` | In-house (custom) |
| Wheel Imbalance Rejection | `SF015A_WhlImbRejctn` | In-house (custom) |
| Vehicle Speed Limiter | `SF016A_VehSpdLimr` | In-house (custom) |
| High Load Stall Limiter | `SF017A_HiLoadStallLimr` | In-house (custom) |
| End of Travel Protection | `SF018A_EotProtn` | In-house (custom) |
| Power Limiter | `SF019B_PwrLimr` | In-house (custom) |
| Handwheel Angle Tracking Servo | `SF020A_HwAgTrakgServo` | In-house (custom) |
| Handwheel Angle Trajectory Generation | `SF021A_HwAgTrajGenn` | In-house (custom) |
| Tuning Selection Authority | `SF023A_TunSelnAuthy` | In-house (custom) |
| End of Travel Protection Firewall | `SF027A_EotProtnFwl` | In-house (custom) |
| Assist High Frequency | `SF028A_AssiHiFrq` | In-house (custom) |
| Stability Compensation | `SF029A_StabyCmp` | In-house (custom) |
| Motor Torque Command Scaling | `SF032A_MotTqCmdSca` | In-house (custom) |
| Vehicle Signal Coding | `SF033A_VehSigCdng` | In-house (custom) |
| Assist Path Firewall | `SF034A_AssiPahFwl` | In-house (custom) |
| Damping Path Firewall | `SF035A_DampgPahFwl` | In-house (custom) |
| Return Path Firewall | `SF036A_RtnPahFwl` | In-house (custom) |
| Limiter Coding | `SF038A_LimrCdng` | In-house (custom) |
| Motor Velocity | `SF040A_MotVel` | In-house (custom) |
| Compliance Error | `SF041A_CmplncErr` | In-house (custom) |
| Handwheel Angle Sensorless | `SF042A_HwAgSnsrls` | In-house (custom) |
| Torque Oscillation | `SF043A_TqOscn` | In-house (custom) |
| Hands On Wheel Detection | `SF044A_HowDetn` | In-house (custom) |
| Handwheel Angle System Arbitration | `SF045A_HwAgSysArbn` | In-house (custom) |
| Torque Loss of Assist | `SF048A_TqLoa` | In-house (custom) |
| Loss of Assist Manager | `SF049A_LoaMgr` | In-house (custom) |
| Motor Torque Translational Damping | `SF050A_MotTqTranlDampg` | In-house (custom) |
| Sensor Offset Learning | `SF051A_SnsrOffsLrng` | In-house (custom) |
| Sensor Offset Correction | `SF052A_SnsrOffsCorrn` | In-house (custom) |
| Handwheel Angle Vehicle Centering Trim | `SF053A_HwAgVehCentrTrim` | In-house (custom) |
| Powerpack Compatibility Check | `SF054A_PwrpkCmpbltyChk` | In-house (custom) |
| Motor Quadrant Detection | `SF101A_MotQuadDetn` | In-house (custom) |
| Motor Control Parameter Estimation | `SF102A_MotCtrlPrmEstimn` | In-house (custom) |
| Motor Reference Model | `SF103A_MotRefMdl` | In-house (custom) |
| Motor Current Regulator Configuration | `SF104A_MotCurrRegCfg` | In-house (custom) |
| Motor Current Regulator Voltage Limiter | `SF105A_MotCurrRegVltgLimr` | In-house (custom) |
| Motor Ripple Cogging Configuration | `SF106A_MotRplCoggCfg` | In-house (custom) |
| Motor Ripple Cogging Command | `SF107A_MotRplCoggCmd` | In-house (custom) |
| Motor Current Peak Estimation | `SF108A_MotCurrPeakEstimn` | In-house (custom) |

</details>

<details>
<summary><strong>Complex Device Drivers — 63 modules</strong> (Complex Device Drivers (CDD))</summary>

Microcontroller configuration, sensing, actuation, power electronics and motor control.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Motor Control Manager | `AR300A_MotCtrlMgr` | In-house (custom) |
| Startup Sequence | `CM100A_StrtUpSeq` | In-house (custom) |
| Exception Handling | `CM101A_ExcpnHndlg` | In-house (custom) |
| Flash Memory | `CM102A_FlsMem` | In-house (custom) |
| Random Access Memory Memory | `CM103A_RamMem` | In-house (custom) |
| Engine Control Module Output And Diagnostics | `CM104A_EcmOutpAndDiagc` | In-house (custom) |
| Microcontroller Unit Core Configuration And Diagnostics | `CM106A_McuCoreCfgAndDiagc` | In-house (custom) |
| Guard Configuration And Diagnostics | `CM107A_GuardCfgAndDiagc` | In-house (custom) |
| Data And Address Parity | `CM108A_DataAndAdrPar` | In-house (custom) |
| Clock Configuration And Mon | `CM109A_ClkCfgAndMon` | In-house (custom) |
| Verify Critical Registers | `CM111A_VrfyCritReg` | In-house (custom) |
| Direct Memory Access Configuration And Use | `CM200A_DmaCfgAndUse` | In-house (custom) |
| Analog to Digital Converter 0 Configuration And Use | `CM300A_ADC0CfgAndUse` | In-house (custom) |
| Adc0 Configuration And Use | `CM300A_Adc0CfgAndUse` | In-house (custom) |
| Adc1 Configuration And Use | `CM320A_Adc1CfgAndUse` | In-house (custom) |
| Analog to Digital Converter Diagnostics | `CM340A_AdcDiagc` | In-house (custom) |
| Sensor Measurement Start | `CM410A_SnsrMeasStrt` | In-house (custom) |
| Tauj0 Configuration And Use | `CM455A_Tauj0CfgAndUse` | In-house (custom) |
| Tauj1 Configuration And Use | `CM460A_Tauj1CfgAndUse` | In-house (custom) |
| Timer Synchronous Generator 31 Configuration And Use | `CM475A_TSG31CfgAndUse` | In-house (custom) |
| Clocked Serial Interface G 0 Configuration And Use | `CM600A_CSIG0CfgAndUse` | In-house (custom) |
| Clocked Serial Interface H 0 Configuration And Use | `CM610A_CSIH0CfgAndUse` | In-house (custom) |
| Motor Ag0 Measurement | `CM620A_MotAg0Meas` | In-house (custom) |
| Clocked Serial Interface H 2 Configuration And Use | `CM630A_CSIH2CfgAndUse` | In-house (custom) |
| Motor Ag1 Measurement | `CM640A_MotAg1Meas` | In-house (custom) |
| Handwheel Tq0 Measurement | `CM650A_HwTq0Meas` | In-house (custom) |
| Handwheel Tq1 Measurement | `CM660A_HwTq1Meas` | In-house (custom) |
| Handwheel Ag1 Measurement | `CM670A_HwAg1Meas` | In-house (custom) |
| Handwheel Tq2 Measurement | `CM680A_HwTq2Meas` | In-house (custom) |
| Handwheel Ag0 Measurement | `CM690A_HwAg0Meas` | In-house (custom) |
| Handwheel Tq3 Measurement | `CM700A_HwTq3Meas` | In-house (custom) |
| Synchronous Cyclic Redundancy Check | `CM800A_SyncCrc` | In-house (custom) |
| Microcontroller Diagnostics | `ES002A_McuDiagc` | In-house (custom) |
| Power Disconnect | `ES003A_PwrDiscnct` | In-house (custom) |
| Power-Up Sequence | `ES004A_PwrUpSeq` | In-house (custom) |
| Temperature Monitor | `ES005A_TmplMonr` | In-house (custom) |
| Non-Volatile Memory | `ES006A_NvM` | In-house (custom) |
| Power Supply | `ES008A_PwrSply` | In-house (custom) |
| System State Mode | `ES100A_SysStMod` | In-house (custom) |
| Diagnostics Manager | `ES101A_DiagcMgr` | In-house (custom) |
| Polarity Configuration | `ES102A_PolarityCfg` | In-house (custom) |
| Calibration Protocol Interface | `ES104A_XcpIf` | In-house (custom) |
| Steering Health Signal Normalization | `ES105A_StHlthSigNormn` | In-house (custom) |
| Steering Health Signal Static | `ES106A_StHlthSigStc` | In-house (custom) |
| Current Measurement | `ES200A_CurrMeas` | In-house (custom) |
| Current Measurement Arbitration | `ES208A_CurrMeasArbn` | In-house (custom) |
| Current Measurement Correlation | `ES209A_CurrMeasCorrln` | In-house (custom) |
| Control Unit Temperature Measurement | `ES210A_EcuTMeas` | In-house (custom) |
| Handwheel Torque Arbitration | `ES228A_HwTqArbn` | In-house (custom) |
| Handwheel Torque Correlation | `ES229A_HwTqCorrln` | In-house (custom) |
| Handwheel Angle Arbitration | `ES238A_HwAgArbn` | In-house (custom) |
| Handwheel Angle Correlation | `ES239A_HwAgCorrln` | In-house (custom) |
| Motor Angle 2 Measurement | `ES241A_MotAg2Meas` | In-house (custom) |
| Motor Angle Comparison | `ES247A_MotAgCmp` | In-house (custom) |
| Motor Angle Arbitration | `ES248A_MotAgArbn` | In-house (custom) |
| Motor Angle Correlation | `ES249A_MotAgCorrln` | In-house (custom) |
| Battery Voltage | `ES250A_BattVltg` | In-house (custom) |
| Battery Voltage Correlation | `ES259A_BattVltgCorrln` | In-house (custom) |
| Sine Voltage Generation | `ES300A_SinVltgGenn` | In-house (custom) |
| Gate Drv0 Control | `ES311A_GateDrv0Ctrl` | In-house (custom) |
| Gate Drv1 Control | `ES312A_GateDrv1Ctrl` | In-house (custom) |
| Motor Drive Diagnostics | `ES320A_MotDrvDiagc` | In-house (custom) |
| Tuning Selection Management | `ES400A_TunSelnMngt` | In-house (custom) |

</details>

<details>
<summary><strong>Basic Software Services — 8 modules</strong> (Basic Software Services (BSW Services))</summary>

Mode management, diagnostics, memory and watchdog services from the Vector MICROSAR stack.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Nexteer Development Error Tracer | `AR998A_NxtrDet` | In-house (custom) |
| Basic Software Mode Manager | `BswM` | Vector-provided |
| Diagnostic Event Manager | `Dem` | Vector-provided |
| Development Error Tracer | `Det` | Vector-provided |
| Electronic Control Unit State Manager | `EcuM` | Vector-provided |
| Non-Volatile Memory | `NvM` | Vector-provided |
| Watchdog Manager | `WdgM` | Vector-provided |
| Universal Measurement and Calibration Protocol | `Xcp` | Vector-provided |

</details>

<details>
<summary><strong>Electronic Control Unit Abstraction — 4 modules</strong> (Electronic Control Unit Abstraction (BSW ECU Abstraction))</summary>

Hardware abstraction: input-output hardware abstraction, memory abstraction, watchdog interface.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Flash EEPROM Emulation | `Fee` | Vector-provided |
| Input Output Hardware Abstraction | `IoHwAb` | Vector-provided, customised |
| Memory Abstraction Interface | `MemIf` | Vector-provided |
| Watchdog Interface | `WdgIf` | Vector-provided |

</details>

<details>
<summary><strong>Microcontroller Abstraction Layer — 8 modules</strong> (Microcontroller Abstraction Layer (MCAL))</summary>

Drivers for the on-chip peripherals: microcontroller unit, ports, digital input-output, serial interfaces, flash, watchdog and Controller Area Network.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Controller Area Network | `Can` | Vector-provided |
| Digital Input Output | `Dio` | Vector-provided |
| Flash | `Fls` | Vector-provided |
| Microcontroller Unit | `Mcu` | Vector-provided |
| Port | `Port` | Vector-provided |
| Renesas Mcal Support | `RenesasMcalSuprt` | Third-party (Renesas) |
| Serial Peripheral Interface | `Spi` | Vector-provided |
| Watchdog | `Wdg` | Vector-provided |

</details>

<details>
<summary><strong>Communication Stack — 5 modules</strong> (Communication Stack (BSW Communication))</summary>

Interaction layer, transport protocol, network management and diagnostics.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| CB Ds | `CBDs` | In-house (custom) |
| Diagnostics | `Diag` | Vector-provided |
| Interaction Layer | `Il` | Vector-provided |
| Network Management | `Nm` | Vector-provided |
| Transport Protocol | `Tp` | Vector-provided |

</details>

<details>
<summary><strong>Operating System and Runtime — 2 modules</strong> (Operating System and Runtime Environment (BSW System))</summary>

Real-time operating system and runtime environment for the software components.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Operating System | `Os` | Vector-provided |
| Runtime Environment | `Rte` | Vector-provided, customised |

</details>

<details>
<summary><strong>Libraries — 9 modules</strong> (Libraries (LIB))</summary>

Shared mathematics, interpolation, fixed-point and filtering libraries plus global-parameter packages.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| Nexteer Mathematics Library | `AR100A_NxtrMath` | In-house (custom) |
| Nexteer Interpolation Library | `AR101A_NxtrIntrpn` | In-house (custom) |
| Nexteer Time Library | `AR102A_NxtrTi` | In-house (custom) |
| Nexteer Fixed-Point Library | `AR103A_NxtrFixdPt` | In-house (custom) |
| Nexteer Filtering Library | `AR104A_NxtrFil` | In-house (custom) |
| Architecture Global Parameters | `AR999A_ArchGlbPrm` | In-house (custom) |
| Cyclic Redundancy Check | `Crc` | Vector-provided |
| Electrical Global Parameters | `ES999A_ElecGlbPrm` | In-house (custom) |
| System Global Parameters | `SF999A_SysGlbPrm` | In-house (custom) |

</details>

<details>
<summary><strong>Tools and Support — 19 modules</strong> (Host-side tools)</summary>

Generators, configurators, static-analysis and support packages that run on the host, not on the controller.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| AUTOSAR Support | `AR200A_ArSuprt` | In-house (custom) |
| AUTOSAR Coupler Support | `AR201A_ArCplrSuprt` | In-house (custom) |
| Microcontroller Support | `AR202A_MicroCtrlrSuprt` | In-house (custom) |
| Nexteer Startup | `AR400A_NxtrStrtUp` | In-house (custom) |
| Quality Assurance for C Support | `TL100A_QACSuprt` | In-house (custom) |
| Component Runtime Environment Generator | `TL101A_CptRteGen` | Vector-provided |
| DaVinci Configurator | `TL102A_Davinci` | Vector-provided |
| Coupler Support | `TL103A_CplrSuprt` | In-house (custom) |
| Generation Year (Vector Configuration Tool) Framework | `TL104A_GENyFramework` | Vector-provided |
| AUTOSAR Template Tool | `TL105A_Artt` | Vector-provided |
| Hex Viewer | `TL106A_HexView` | Vector-provided |
| Polyspace Static Analysis Support | `TL108A_PolyspaceSuprt` | In-house (custom) |
| Common Checks Tool | `TL111A_CmnChksTool` | In-house (custom) |
| Python Tooling | `TL112A_Python` | In-house (custom) |
| Manufacturing Services Support | `TL113A_MfgSrvSuprt` | In-house (custom) |
| Release Note Generator | `TL115A_RelsNoteGenr` | In-house (custom) |
| Software Option Switch | `TL116A_SwOptnSwt` | In-house (custom) |
| Data Dictionary | `TL117A_DataDict` | In-house (custom) |
| Vector Bsw Support | `VectorBswSuprt` | Vector-provided |

</details>

<details>
<summary><strong>System Integration — 3 modules</strong> (Integration)</summary>

Top-level integration project wiring the configured stack for the controller and vehicle platform.

| Module (long name) | Repository short name | Origin |
|---|---|---|
| General Motors T1XX Platform Microcontroller Unit Configuration | `CM010A_GmT1xxMcuCfg` | In-house (custom) |
| Electronic Control Unit Configuration | `EcuC` | Vector-provided, customised |
| General Motors T1XX Platform EPS RH 850 | `GM_T1XX_EPS_RH850` | Joint integration (Vector + in-house) |

</details>

## Vector-Provided Code versus In-House Code

Third-party code from **Vector Informatik (MICROSAR stack, DaVinci Configurator, GENy)** is kept separate from **in-house developed** steering and driver code:

- **Vector-provided** modules (Microcontroller Abstraction Layer drivers, operating system, memory stack, diagnostics, communication stack) are used as delivered plus generated configuration. Do not hand-edit generated output (`generate/` folders, `GenData` artefacts); regenerate with the tool noted on the module page.
- **In-house (custom)** modules (all steering functions, customer functions, complex device drivers, message proxies, manufacturing services) carry the project implementation, design documents and tests.
- **Vector-provided, customised** modules combine a Vector base with project-specific code (Input Output Hardware Abstraction, Runtime Environment configuration, Electronic Control Unit Configuration).
- The **Renesas** microcontroller support package comes from the hardware vendor.
- The **top-level integration project** (`GM_T1XX_EPS_RH850`) wires Vector and in-house parts together.

Every module page in the documentation site carries an origin badge with the evidence used to classify it.

## Documentation Site

The `docs/` folder at the repository root is a self-contained **Astro v7 + Starlight** project. It documents every AUTOSAR layer and module, distinguishes Vector-provided from in-house code, and publishes Markdown converted from the Word and PDF files shipped inside the module `doc` folders.

```bash
cd docs
npm install     # install Astro and Starlight
npm run dev     # local preview with hot reload
npm run build   # production build into docs/dist/
```

Deployment to GitHub Pages uses the `docs/dist/` output. The site URL and base path are **derived automatically** from the `GITHUB_REPOSITORY` environment variable or the `origin` git remote in `docs/astro.config.mjs`, so forks need no configuration changes and no user or repository name is hardcoded anywhere.

## Installation and Build

### Host prerequisites

1. Green Hills Software MULTI toolchain for Renesas RH850.
2. Vector DaVinci Configurator and GENy for AUTOSAR configuration and generation.
3. Python tooling (see the Python tools package) and the module integration scripts.
4. Quality Assurance for C and Polyspace for static analysis (optional but recommended).

### Build steps

1. Clone this repository.
2. Generate the Runtime Environment and Basic Software configuration with DaVinci/GENy (see [Tools and Support](docs/src/content/docs/tools-and-support/index.md)).
3. Run the per-module integration scripts (`tools/Integrate.bat`) via the top-level integration project (`GM_T1XX_EPS_RH850`).
4. Compile with the Green Hills projects (`*.gpj`) and link the firmware image.
5. Flash the image onto the Renesas RH850 controller.

See the [build system](docs/src/content/docs/overview/build-system.md) page for the full workflow.

## General Motors T1XX Platform

The **General Motors T1XX** platform is an advanced electronic architecture for General Motors vehicles. Examples of vehicles based on the T1XX platform:

1. **Chevrolet Silverado**: a full-size pickup truck known for its robust performance and capability.
2. **GMC Sierra**: similar to the Silverado, the Sierra offers upscale features and a premium driving experience.
3. **Cadillac Escalade**: a luxury sport-utility vehicle with a spacious interior, advanced technology and sophisticated design.
4. **Chevrolet Tahoe**: a full-size sport-utility vehicle offering versatility, comfort and ample seating.
5. **GMC Yukon**: similar to the Tahoe, the Yukon provides a refined driving experience and upscale features.
6. **Chevrolet Suburban**: a longer version of the Tahoe with even more cargo space and passenger seating.
7. **Cadillac CT4**: a compact luxury sedan balancing performance, comfort and style.

## Contributing

We encourage contributions! If you would like to improve this project, please submit a pull request. Keep Vector-provided files pristine, regenerate (do not hand-edit) generator output, and expand abbreviations to long names in documentation.

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for the full text.
