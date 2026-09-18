---
title: "Non-Volatile Memory (ES006A_NvM)"
description: "Non-Volatile Memory: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Non-Volatile Memory component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES006A_NvM_Design` | Design package |
| `ES006A_NvM_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES006A_NvM_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES006A_NvM_Impl` |  |
| C sources | `CDD_NvMProxy.c`, `CDD_NvMProxyApi.c`, `CDD_NvMProxyNonRte.c` |
| Public headers | `CDD_NvMProxy.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NvMProxy.dcf`, `NvMProxy_attr_def.xml`, `NvMProxy_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `CDD_NvMProxyDftDataGroup.h.tt`, `CDD_NvMProxy_Cbk.c.tt`, `CDD_NvMProxy_Cbk.h.tt`, `CDD_NvMProxy_Cfg.c.tt`, `CDD_NvMProxy_Cfg.h.tt`, `CDD_NvMProxy_Cfg_private.h.tt`, `NvMProxy_Generate.bat`, `NvMProxy_swc.arxml.tt` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `DVCfgCmd.log`, `ES006A_NvM_Impl.gpj`, `Integrate.bat`, `NvMProxy.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `ES006A_NvM_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `ES006A_NvM_Impl/src/CDD_NvMProxy.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES006A_NvM_Impl/src/CDD_NvMProxyApi.c`, `ES006A_NvM_Impl/src/CDD_NvMProxyNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES006A_NvM_FDD.docx`

- **Source path in repository:** `ES006A_NvM_Design/Doc/ES006A_NvM_FDD.docx`
- **Format:** `.docx`
- **Size:** `443 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

**Converted content:**

Non Volatile RAM Manager And

Non Volatile RAM Manager Proxy

FDD #ES-006A

Contents

1.High Level Description4

2.Derived Requirements4

3.Sub-Function Data Flow4

4.Design Rationale5

5.Components6

5.1.NvM: Non Volatile Memory (AUTOSAR BSW)6

5.1.1.BSW Configuration6

5.1.1.1.NvMCommon6

5.1.2.Periodic Functions7

5.1.2.1.NvM_MainFunction7

5.1.2.1.1.Function Definition7

5.1.3.Service Sub-Functions8

5.1.3.1.API Configuration Class 19

5.1.3.1.1.Sub-Function: NvM_Init9

5.1.3.1.2.Sub-Function: NvM_ReadAll10

5.1.3.1.3.Sub-Function: NvM_WriteAll11

5.1.3.1.4.Sub-Function: NvM_GetErrorStatus12

5.1.3.1.5.Sub-Function: NvM_SetRamBlockStatus13

5.1.3.1.6.Sub-Function: NvM_CancelWriteAll14

5.1.3.2.API Configuration Class 215

5.1.3.2.1.Sub-Function: NvM_SetDataIndex15

5.1.3.2.2.Sub-Function: NvM_GetDataIndex16

5.1.3.2.3.Sub-Function: NvM_ReadBlock17

5.1.3.2.4.Sub-Function: NvM_WriteBlock18

5.1.3.2.5.Sub-Function: NvM_RestoreBlockDefaults19

5.1.3.2.6.Sub-Function: NvM_CancelJobs20

5.1.3.3.API Configuration Class 321

5.1.3.3.1.Sub-Function: NvM_SetBlockProtection21

5.1.3.3.2.Sub-Function: NvM_EraseNvBlock22

5.1.3.3.3.Sub-Function: NvM_InvalidateNvBlock23

5.1.4.Type Definitions24

5.1.4.1.Std_ReturnType24

5.1.4.2.NvM_RequestResultType24

5.1.4.3.NvM_BlockIdType25

5.2.NvM_Proxy: Non Volatile Memory Proxy (Nexteer CDD)26

5.2.1.Design Rationale26

5.2.2.Sub-Functions26

5.2.2.1.Sub-Function: NvMProxy_Init26

5.2.2.1.1.Hardware Related Design26

5.2.2.1.2.Software Related Design26

6.Timing / Execution Constraints27

6.1.Rationale / Comments27

6.2.Rates and State Execution: NvM27

6.3.Rates and State Execution: NvMProxy28

7.Serial Communications Interfaces28

8.Additional Information29

8.1.NvM block definition Considerations29

8.1.1.Scenario 129

8.1.2.Scenario 229

8.2.Software Component Design Considerations30

8.2.1.API Port Selection30

9.Revision Record & Change Approval31

## High Level Description

This design document describes the functionality, API, and the configuration of the AUTOSAR basic software (BSW) module NVRAM Manager (NvM) and the NvM Proxy (NvMProxy).

The NvM provides services to ensure the data storage and maintenance of NV (non-volatile) data. The NvM module is able to administrate the NV data for an EEPROM and/or a Flash EEPROM Emulation (FEE) device.

The NvMProxy provides an interface for software components outside of the application of the NvM to communicate with the NvM component.

## Derived Requirements

None

## Sub-Function Data Flow

None

## Design Rationale

The NvM and NvMProxy components are integrated below the application layer in the basic software layer of the AUTOSAR model.

NvMProxy was designed so that all software components can send their NvM requests to the proxy interface, which will communicate the request to the NvM and report the results back to the calling component. This simplifies the design of software components by only requiring one interface for defining NvM needs and providing the needed functionality to switch the OS context in the event the calling application is different than the application NvM is integrated.

## Components

The following sections describe the NvM and NvM proxy components.

### NvM: Non Volatile Memory (AUTOSAR BSW)

#### BSW Configuration

#### NvMCommon

| Configuration Parameter | Value | Rationale |

| --- | --- | --- |

| API Configuration Class | MVM_API_CONFIG_CLASS_ 3 | Class 3 shall be used  to provide all API options  to software components. This is to prevent rework of existing components if use cases change and require API functions that may not have been available during component development under a different API class. |

| Compiled Configuration Id | 1 | Version of the NV memory layout, always shall start at 1 and be revised if the memory layout changes |

| Crc  Number of Bytes | 64 | Dummy value, not used. |

| Dataset Selection Bits | 1 | Shall be set to 1 if the only block types are “native” and “redundant.” If a dataset is required, then the number needs to be set satisfy the following equation:  2^(Selection Bits) >= max(dataset) For example,  if the largest dataset for all configured blocks  was 30, the selection bits  are  required to be  set to 5.  2^5 = 32 >= 30 |

| Development Error Detection | FALSE | Only should be true for early development . Shall not be used in production level software |

| Drivers Mode Switch | True | Disables processing of background sector switching from startup and shutdown events. |

| Dynamic Configuration  Handling | True | Allows for adapting new FEE layouts over existing layouts . See  section  5.1.3.2.2  for details on the impact of this setting. |

| Job Prioritization | False | No requirement for prioritization of any blocks |

| Maximum Number of Write Retries | 3 | Default setting |

| Multi Block Callback | NvMProxy_MultiBlkCallBack |  |

| Multi block Job Status Information | False |  |

| Polling Mode | True | Enabled to provide the application the ability to poll the status of the asynchronous request. |

| Repeat Mirror Operations | 0 | Default setting |

| SetRamBlockStatus  API | True | Applications shall use  SetRamBlockStatus  API to indicate their RAM shadows have updated. |

| Size Of Immediate Status Information | N/A | Not used |

| Size Of Standard Job Queue | 8 | Default setting |

| Version Information API | False | N/A |

Configuration Parameter

Value

Rationale

API Configuration Class

MVM_API_CONFIG_CLASS_3

Class 3 shall be used to provide all API options to software components. This is to prevent rework of existing components if use cases change and require API functions that may not have been available during component development under a different API class.

Compiled Configuration Id

1

Version of the NV memory layout, always shall start at 1 and be revised if the memory layout changes

Crc Number of Bytes

64

Dummy value, not used.

Dataset Selection Bits

1

Shall be set to 1 if the only block types are “native” and “redundant.” If a dataset is required, then the number needs to be set satisfy the following equation:

2^(Selection Bits) >= max(dataset)

For example, if the largest dataset for all configured blocks was 30, the selection bits are required to be set to 5. 2^5 = 32 >= 30

Development Error Detection

FALSE

Only should be true for early development. Shall not be used in production level software

Drivers Mode Switch

True

Disables processing of background sector switching from startup and shutdown events.

Dynamic Configuration Handling

True

Allows for adapting new FEE layouts over existing layouts. See section 5.1.3.2.2 for details on the impact of this setting.

Job Prioritization

False

No requirement for prioritization of any blocks

Maximum Number of Write Retries

3

Default setting

Multi Block Callback

NvMProxy_MultiBlkCallBack

Multi block Job Status Information

False

Polling Mode

True

Enabled to provide the application the ability to poll the status of the asynchronous request.

Repeat Mirror Operations

0

Default setting

SetRamBlockStatus API

True

Applications shall use SetRamBlockStatus API to indicate their RAM shadows have updated.

Size Of Immediate Status Information

N/A

Not used

Size Of Standard Job Queue

8

Default setting

Version Information API

False

N/A

#### Periodic Functions

#### NvM_MainFunction

This function has to be called cyclically. It is the entry point for the NvM component. In this function processing of all asynchronous jobs are handled (read/write/erase/invalidate/CRC calculation).

#### Function Definition

| Prototype |

| --- |

| void  NvM_MainFunction  ( void ) |

| Parameter |

| N/A |

| Return Code |

| N/A |

Prototype

void NvM_MainFunction ( void )

Parameter

N/A

Return Code

N/A

#### Service Sub-Functions

The value of the API configuration class determines which API server ports are available to the system. The image below shows the breakdown of the functionality for each API Configuration Class.

In the following sub sections, the APIs are defined for application software components (SWCs) and BSW components. The application function definition shall be used for components that sit above the RTE layer in the AUTOSAR model. The RTE generator will absorb some of the dynamic arguments, such as BlockId, and create a macro with the proper definition for the software component. Complex device drivers and other BSWs that sit below the RTE layer shall use the CDD function definition.

#### API Configuration Class 1

The following sections contain a description of the functions provided by the AUTOSAR NvM basic software component with API Configuration Class 1 configured.

#### Sub-Function: NvM_Init

#### Hardware Related Design

None

#### Software Related Design

| Function  Particularities |  |

| --- | --- |

| Request Type | Synchronous |

| Re-entrant | Yes |

| Expected Caller Context | Shall only be called from ECU state manager or equivalent function. |

Function Particularities

Request Type

Synchronous

Re-entrant

Yes

Expected Caller Context

Shall only be called from ECU state manager or equivalent function.

Before the NvM component can be used, it has to be initialized. Depending on the program the NvM is integrated, the BSWs from lower levels shall be initialized prior to the NvM. The table below is an example of this strategy for Fee and Ea use cases for initialize modules from the low level components up to the NvM.

|  | Fee | Ea |

| --- | --- | --- |

| Low level driver | Fls | SPI /EEP |

| Device Abstraction | FEE | EA |

| Non-Volatile Manager | NvM |  |

Fee

Ea

Low level driver

Fls

SPI/EEP

Device Abstraction

FEE

EA

Non-Volatile Manager

NvM

The NvM AUTOSAR component compliant with ASIL-D standards, NvM_Init shall be called as a trusted function. This will allow the NvM_Init function access to all the permanent RAM shadows defined in software, regardless of their ASIL rating. This reduces the RAM and throughput during start up to move data from application to another.

#### Application Function Definition

None

#### CDD Function Definition

| Prototype |

| --- |

| void  NvM_Init  ( void ) |

| Parameter |

| N/A |

| Return Code |

| N/A |

Prototype

void NvM_Init ( void )

Parameter

N/A

Return Code

N/A

#### Sub-Function: NvM_ReadAll

#### Hardware Related Design

None

#### Software Related Design

| Function  Particularities |  |

| --- | --- |

| Request Type | Asynchronous |

| Re-entrant | No |

| Expected Caller Context | Shall only be called from ECU state manager or equivalent function. |

Function Particularities

Request Type

Asynchronous

Re-entrant

No

Expected Caller Context

Shall only be called from ECU state manager or equivalent function.

This function shall only be called after NvM_Init has been executed. The request loads all the RAM blocks that have the option NVM_SELECT_BLOCK_FOR_READALL selected.

Note: Non-permanent blocks and data set blocks are skipped during execution of this function and must be loaded manually by calling NvM_ReadBlock().

During the execution of NvM_ReadAll(), the value in the configuration ID (block 1) is compared with the compiled ID version in the NvM settings. With the Dynamic Configuration Handling option set to True, any NvM blocks with the option Resistant to Changed Software enabled will be processed and loaded into RAM as if the configuration IDs matched. If the option Resistant to Changed Software is not enabled, the blocks will be treated is if they were invalid or blank.

#### Application Function Definition

None

#### CDD Function Definition

| Prototype |

| --- |

| void  NvM_ ReadAll  ( void ) |

| Parameter |

| N/A |

| Return Code |

| N/A |

Prototype

void NvM_ReadAll ( void )

Parameter

N/A

Return Code

N/A

#### Sub-Function: NvM_WriteAll

#### Hardware Related Design

None

#### Software Related Design

| Function  Particularities |  |

| --- | --- |

| Request Type | Asynchronous |

| Re-entrant | No |

| Expected Caller Context | Shall only be called from ECU state manager or equivalent function. |

Function Particularities

Request Type

Asynchronous

Re-entrant

No

Expected Caller Context

Shall only be called from ECU state manager or equivalent function.

Request to write all blocks with RAM data that has been changed and have the option NVM_SELECT_BLOCK_FOR_WRITEALL selected.

Note: Non-permanent blocks and data set blocks are skipped during execution of this function and must be written manually by calling NvM_WriteBlock().


*... content truncated for brevity; see the source document in the repository. ...*

### `ES006A_NvM_DDReport.txt`

- **Source path in repository:** `ES006A_NvM_Design/Reports/ES006A_NvM_DDReport.txt`
- **Format:** `.txt`
- **Size:** `13 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES006A_NvM_DataDict
07-Oct-2016 09:55:24
Tool Release:  2.48.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF099A
--------------------------------------------------------------
(variable: 1, errors: 0)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
Missing Model 	Unable to find model for comparison to data dictionary.
(errors:  1)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
NvM_Init                    	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
NvM_Init                    	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvM_MainFunction            	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
NvM_MainFunction            	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvM_MainFunction            	    Main           Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvM_MainFunction            	    Function       Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 4, errors: 6)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
NvMPIM_EraseBlock           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_EraseBlock           	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_EraseBlock           	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_EraseBlock           	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetDataIndex         	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_GetDataIndex         	.TestTolerance 	Value is at default value of 999.
NvMPIM_GetDataIndex         	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetDataIndex         	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetDataIndex         	    Index          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetErrorStatus       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_GetErrorStatus       	.TestTolerance 	Value is at default value of 999.
NvMPIM_GetErrorStatus       	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetErrorStatus       	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetErrorStatus       	    Error          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_GetErrorStatus       	    Status         Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_InvalidateBlock      	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_InvalidateBlock      	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_InvalidateBlock      	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_InvalidateBlock      	    Invalidate     Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_InvalidateBlock      	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_ReadBlock            	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_ReadBlock            	.TestTolerance 	Value is at default value of 999.
NvMPIM_ReadBlock            	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_ReadBlock            	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_ReadBlock            	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_RestoreBlockDefaults 	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_RestoreBlockDefaults 	.TestTolerance 	Value is at default value of 999.
NvMPIM_RestoreBlockDefaults 	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_RestoreBlockDefaults 	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_RestoreBlockDefaults 	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_RestoreBlockDefaults 	    Defaults       Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetBlockProtection   	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_SetBlockProtection   	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetBlockProtection   	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetBlockProtection   	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetBlockProtection   	    Protection     Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetDataIndex         	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_SetDataIndex         	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetDataIndex         	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetDataIndex         	    Index          Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetRamBlockStatus    	.SrvRunnnable:	Name should not contain FDDs <ShoName>
NvMPIM_SetRamBlockStatus    	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetRamBlockStatus    	    M_             Unknown Keyword used.Only Nexteer approved Keywords should be used.
NvMPIM_SetRamBlockStatus    	    Block          Unknown Keyword used.Only Nexteer approved Keywords should be used.
```
*... truncated (127 more lines in the source file). ...*

### `ES006A_NvM_Integration_Manual.doc`

- **Source path in repository:** `ES006A_NvM_Impl/doc/ES006A_NvM_Integration_Manual.doc`
- **Format:** `.doc`
- **Size:** `152 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
