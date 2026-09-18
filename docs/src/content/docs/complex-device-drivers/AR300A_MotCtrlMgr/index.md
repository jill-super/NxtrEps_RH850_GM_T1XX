---
title: "Motor Control Manager (AR300A_MotCtrlMgr)"
description: "Motor Control Manager: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Motor Control Manager component belongs to **Motor Control Management** in the **Complex Device Drivers** layer. It coordinates the motor-control software as a complex device driver.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `AR300A_MotCtrlMgr_Design` | Design package |
| `AR300A_MotCtrlMgr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR300A_MotCtrlMgr_Design` |  |
| Documentation folders | `Doc/`, `Design/` |
| `AR300A_MotCtrlMgr_Impl` |  |
| Public headers | `CDD_MotCtrlMgr_Irq.h`, `MotCtrlMgr_MemMap.h` |
| AUTOSAR model | `CDD_MotCtrlMgr_bswmd.arxml` |
| Generator output | `AR300A_MotCtrlMgr_DataDict.m.tt`, `CDD_MotCtrlMgr.c.tt`, `CDD_MotCtrlMgr_Data.c.tt`, `CDD_MotCtrlMgr_Data.h.tt`, `CDD_MotCtrlMgr_Irq.c.tt`, `MotCtrlMgr_Generate.bat` |
| Tooling and integration scripts | `AR300A_MotCtrlMgr_Impl.gpj`, `CreateGHSProject.bat`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (1 file(s), e.g. `AR300A_MotCtrlMgr_Impl/autosar/CDD_MotCtrlMgr_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AR300A_MotCtrlMgr_FDD.docx`

- **Source path in repository:** `AR300A_MotCtrlMgr_Design/Design/AR300A_MotCtrlMgr_FDD.docx`
- **Format:** `.docx`
- **Size:** `262 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

**Converted content:**

Motor Control Manager

FDD #AR300A

.

1.High Level Description4

2.Derived Requirements4

3.Function I/O5

3.1.Data Ownership5

3.2.Input Description5

3.3.Output Description6

3.4.Sub-Function Data Flow7

4.Design Rationale and Assumptions8

5.Sub-Functions8

5.1.Sub-Function: MotCtrlMgrPer1 – Motor Control To 2ms RTE interface8

5.1.1.Hardware Related Design8

5.1.2.Software Related Design9

5.1.3.Sub Function Calibrations9

5.1.4.Signal Availability9

5.2.Sub-Function:  MotCtrlMgrPer2 –2ms RTE to Motor Control interface9

5.2.1.Hardware Related Design9

5.2.2.Software Related Design9

5.2.3.Sub Function Calibrations10

5.2.4.Signal Availability10

5.3.Sub-Function:  MotCtrlMgrIrq: Motor Control Interrupt Service Routine10

5.3.1.Hardware Related Design10

5.3.2.Software Related Design10

5.3.3.Sub Function Calibrations10

5.3.4.Signal Availability10

5.4.Sub-Function:  Definition of Motor Control Data10

5.4.1.Hardware Related Design10

5.4.2.Software Related Design10

5.4.3.Sub Function Calibrations11

5.4.4.Signal Availability11

5.5.Sub-Function:  Non-RTE Enumeration Definitions12

5.5.1.Hardware Related Design12

5.5.2.Software Related Design12

5.5.3.Sub Function Calibrations12

5.5.4.Signal Availability12

5.6.Sub-Function:  Motor Control Data Access Macros12

5.6.1.Hardware Related Design12

5.6.2.Software Related Design12

5.6.3.Sub Function Calibrations12

5.6.4.Signal Availability13

5.7.Sub-Function:  Motor Control Data Signal Mapping13

5.7.1.Hardware Related Design13

5.7.2.Software Related Design13

5.7.3.Sub Function Calibrations13

5.7.4.Signal Availability13

6.Timing / Execution Constraints13

6.1.Rationale / Comments13

6.2.Rates and State Execution14

7.Serial Communications Interfaces14

8.Additional Information14

9.Revision Record & Change Approval15

## High Level Description

The Motor Control Manager component is responsible for three major tasks:

Defining and owning the Motor Control Interrupt routine

Defining and owning all Motor Control related global signals that are not handled by the RTE including providing interfaces for component access to these signals

Providing a standardized interface between the Motor Control related global signals and the RTE signals

## Derived Requirements

None

## Function I/O

### Data Ownership

The following table shows the data that the MotCtrlMgr is expected to define and own.  Please note that only a subset of this data is explicitly used as I/O for the MotCtrlMgr subfunctions.

| Data | Description |

| --- | --- |

| MotCtrlMgr_MotCtrlToTwoMilliSec_Rec | Structure containing all of the signals that are written by motor control scheduled  runnables  that are required to  be read   by 2ms RTE scheduled  runnables .   T his structure is the structure that the Motor Control  Runnables  write to.   The list of signals contained in this structure can change from program to program based on program dataflow requirements. |

| MotCtrlMgr_TwoMilliSecFromMotCtrl_Rec | Structure containing all of the signals that are written by motor control scheduled  runnables  that are required to be read by 2ms RTE scheduled  runnables .   T his structure is the structure that the 2ms RTE scheduled  runnables  read from.  The list of signals contained in this structure can change from program to program based on program dataflow requirements. |

| MotCtrlMgr_TwoMilliSecToMotCtrl_Rec | Structure containing all of the signals that are written by 2ms RTE scheduled  runnables  that are required to be read by motor control scheduled  runnables .  This structure is the structure that the 2ms RTE scheduled  runnables  write to. The list of signals contained in this structure can change from program to program based on program dataflow requirements. |

| MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec | Structure containing all of the signals that are written by 2ms RTE scheduled  runnables  that are required to be read by motor control scheduled  runnables .  This structure is the structure that the Motor Control  Runnables  read from. The list of signals contained in this structure can change from program to program based on program dataflow requirements. |

| MotCtrlMgr_MotCtrlInt_Rec | Structure containing all of the signals that read and written only by motor control scheduled  runnables  (i.e. no interface with RTE scheduled  runnables  required).  The list of signals contained in this structure can change from program to program based on program dataflow requirements. |

## Data

## Description

MotCtrlMgr_MotCtrlToTwoMilliSec_Rec

Structure containing all of the signals that are written by motor control scheduled runnables that are required to be read by 2ms RTE scheduled runnables.  This structure is the structure that the Motor Control Runnables write to.  The list of signals contained in this structure can change from program to program based on program dataflow requirements.

MotCtrlMgr_TwoMilliSecFromMotCtrl_Rec

Structure containing all of the signals that are written by motor control scheduled runnables that are required to be read by 2ms RTE scheduled runnables.  This structure is the structure that the 2ms RTE scheduled runnables read from. The list of signals contained in this structure can change from program to program based on program dataflow requirements.

MotCtrlMgr_TwoMilliSecToMotCtrl_Rec

Structure containing all of the signals that are written by 2ms RTE scheduled runnables that are required to be read by motor control scheduled runnables.  This structure is the structure that the 2ms RTE scheduled runnables write to. The list of signals contained in this structure can change from program to program based on program dataflow requirements.

MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec

Structure containing all of the signals that are written by 2ms RTE scheduled runnables that are required to be read by motor control scheduled runnables.  This structure is the structure that the Motor Control Runnables read from. The list of signals contained in this structure can change from program to program based on program dataflow requirements.

MotCtrlMgr_MotCtrlInt_Rec

Structure containing all of the signals that read and written only by motor control scheduled runnables (i.e. no interface with RTE scheduled runnables required).  The list of signals contained in this structure can change from program to program based on program dataflow requirements.

### Input Description

The following inputs are used by this FDD.  Source FDD, range, resolution are located in the FDD data dictionary.

| Input  Name | Description |

| --- | --- |

| MotCtrlMgr_TwoMilliSecFromMotCtrl_Rec | See description above |

| <Signal1>…<Signal # > | All  RTE  signals coming from the  2ms RTE  scheduled  runnables  that are required to be read by motor control scheduled  runnables .   The list of signals can change from program to program based on program dataflow requirements. |

## Input Name

## Description

MotCtrlMgr_TwoMilliSecFromMotCtrl_Rec

See description above

<Signal1>…<Signal#>

All RTE signals coming from the 2ms RTE scheduled runnables that are required to be read by motor control scheduled runnables.  The list of signals can change from program to program based on program dataflow requirements.

### Output Description

The following outputs are generated by this FDD.  Source FDD, range, resolution are located in the FDD data dictionary.

| Output  Name | Description |

| --- | --- |

| MotCtrlMgr_TwoMilliSecToMotCtrl_Rec | See description above |

| < Signal A >…< Signal X > | All  RTE  signals  being read by  2ms RTE  scheduled  runnables  that are  written  by motor control scheduled  runnables .   The list of signals can change from program to program based on program dataflow requirements. |

## Output Name

## Description

MotCtrlMgr_TwoMilliSecToMotCtrl_Rec

See description above

<SignalA>…<SignalX>

All RTE signals being read by 2ms RTE scheduled runnables that are written by motor control scheduled runnables.  The list of signals can change from program to program based on program dataflow requirements.

### Sub-Function Data Flow

## Design Rationale and Assumptions

The Motor Control Manager component is intended to provide a flexible design that will allow a consistent definition of all of the Motor Control related global signals, the Motor Control interrupt routine, and the interface between the Motor Control global signals and the RTE.  The design is also partially influenced on the knowledge of how the DMA, ADC, and TSG3 hardware peripherals will be used for electrical architecture 4.  The following assumptions were considered in the design, and further details on some of these items can be found later in this document:

The ADC0 will be used primarily for Motor Control ADC reads and the ADC1 will be used for 2ms ADC reads.  The 2ms ADC reads will require explicit transfer from the Motor Control time domain to the 2ms time domain.

The DMA will be transferring ADC results from ADC result registers into RAM and therefore the ADC result RAM signals must be packed together in proper order.  Additionally, all ADC results registers will be transferred, not just those that are used in a program.

The DMA will be transferring TSG3 PWM signals from RAM to TSG3 registers and therefore must be packed together in proper order.  The signals names and ordering are as follows:

MotCtrlTSG3nDCMP0E, MotCtrlTSG3nCMP0E, MotCtrlTSG3nCMP12E

MotCtrlTSG3nCMPWE, MotCtrlTSG3nCMPVE, MotCtrlTSG3nCMPUE

All signals being transferred between the Motor Control and 2ms time domains will be done through the DMA and will require definition of signals for both time domains.  This is why these signals are all packed together in a structure.  Additionally, it is assumed that the DMA will be using 128 bit transfers for this data, and memory alignment and size of the structure are designed accordingly.

It is assumed that the RAM data structures that the DMA will be writing to will need to be placed in an isolated RAM location in memory and will therefore need special provisions to allow specific placement of this data in memory.  It is also assumed the DMA will not have any specific restrictions on memory that it can read from.

Signals owned by the Motor Control Manager are not required to be defined as a structure.  Enumerations, however, will be supported, but only for underlying datatypes of uint8, uint16, uint32.

The current design assumes only a 2ms interface to RTE is required

## Sub-Functions

### Sub-Function: MotCtrlMgrPer1 – Motor Control To 2ms RTE interface

#### Hardware Related Design

None

#### Software Related Design

#### Sub Function Calibrations

None

#### Signal Availability

None

### Sub-Function:  MotCtrlMgrPer2 –2ms RTE to Motor Control interface

#### Hardware Related Design

None

#### Software Related Design

#### Sub Function Calibrations

None

#### Signal Availability

None

### Sub-Function:  MotCtrlMgrIrq: Motor Control Interrupt Service Routine

#### Hardware Related Design

None

#### Software Related Design

The motor control interrupt routine needs to be configurable to allow flexibility in the runnable list that it contains as well as the order in which the runnables are called.   Additionally, it will contain a loop counter that will toggle between 0 and 1 every motor control loop.  Any runnables that need to be scheduled at a rate of MotorControlx2 will only run when the counter is equal to 1, whereas runnables that need to be scheduled at a rate of MotorControl will run regardless of the counter value.  The counter should be initialized to 1 and will toggle after all runnables are executed.

#### Sub Function Calibrations

None

#### Signal Availability

None

### Sub-Function:  Definition of Motor Control Data

#### Hardware Related Design

None

#### Software Related Design

This sub-function defines the details of how the process for defining the motor control related signals contained in the Data Ownership section above.  There are some high level details that hold true for all signals as follows:

Structures are used to implement the different data categories to group all of the data together

All structure elements are defined to pack the data into a structure in the most efficient manner.  This involves grouping all of the same size datatypes together in the structure as well as grouping the different size groups in descending order of size (i.e. 32bit->16bit->8bit).


*... content truncated for brevity; see the source document in the repository. ...*

### `MotCtrlMgr Integration Manual.doc`

- **Source path in repository:** `AR300A_MotCtrlMgr_Impl/doc/MotCtrlMgr Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `172 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotCtrlMgr_MDD.doc`

- **Source path in repository:** `AR300A_MotCtrlMgr_Impl/doc/MotCtrlMgr_MDD.doc`
- **Format:** `.doc`
- **Size:** `188 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotCtrlMgr DataDictionary Tool User Guide.docx`

- **Source path in repository:** `AR300A_MotCtrlMgr_Impl/tools/DataDictionary/MotCtrlMgr DataDictionary Tool User Guide.docx`
- **Format:** `.docx`
- **Size:** `102 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

## Purpose

This document provides details on using the DataDictionary.exe tool for generating and testing the MotCtrlMgr component.

## Overview

The MotCtrlMgr component is a project specific, highly configurable component.  The majority of the configuration parameters of the component, however, can be derived from analysis of the collection of data dictionaries that exist within any given project.  A tool was created (DataDictionary.exe) to create a file which contains the bulk of the MotCtrlMgr configuration which can subsequently be imported into the AUTOSAR Configuration Tools (Davinci Configurator).  While this tool can primarily be used at a project configuration level, it also is used at a component level in the MotCtrlMgr component.  The usage at a component level serves two primary purposes:

Generation of the majority of the MotCtrlMgr “test” configuration.

MotCtrlMgr component defines a “test” configuration.  This test configuration is used for several purposes:

To exercise the .bswmd file containing the configuration parameters of MotCtrlMgr (for property correctness and Davinci Configuration compatibility)

To test for the proper/successful generation of the MotCtrlMgr component’s generated configuration files

To generate test files of all generated files of this component used to run static analysis checks on the generated file output, provide the possibility for unit testing of the generated files, and test compilation of the generated files.

Test of the DataDictionary.exe tool output.

Since the DataDictionary.exe tool is used at a project level with files that will change from project to project as needed, it is useful to have a fixed, known set of test files as inputs to the tool to test that the tool is providing the correct output with a known set of inputs.  These input files can also be tailored to test different combinations of input scenarios to try to provide a robust set of test inputs to the tool.

## Usage Steps for MotCtrlMgr Component Development

Unzip TestDataManagement.zip file into AR300A_MotCtrlMgr_Impl\tools\DataDictionary directory

This is needed since Telelogic synergy can’t currently recognize some of the folder names that are in this directory.

Update Data Dictionary input files in AR300A_MotCtrlMgr_Impl\tools\DataDictionary directory

This step is required if there are new or changed configurations that need to be tested.  This step would be manually changing the .m files to add or change the configuration or this could also be done with the aid of matlab data dictionary tools.

Note: if new configurations include new/changed enumerations, these enumerations will need to be manually added into the “TestDataManagement” folder that was unzipped in step 1. And this update will need to be re-zipped for check-in to Synergy.

Note: if the new configurations include new signal mappings, the Mappings.xml file will need to be manually updated in the AR300A_MotCtrlMgr_Impl\tools\DataDictionary directory.

Rerun tool: AR300A_MotCtrlMgr_Impl\tools\DataDictionary\DataDictionary.exe to create new configuration file needed for the next step

Select “Cals” option from initial Data Dictionary tool options:

Select proper tools settings for generation of MotCtrlMgr configuration file.  (note file paths may not be exactly the same as listed below):

Select “Generate” option in tool to create MotCtrlMgr.arxml configuration file.

Import MotCtrlMgr.arxml into MotCtrlMgr component Davinci Configurator project.

Notes:  It is suggested to remove all configuration containers manually from the old configuration before importing the updated configuration.  This allows easier import to ensure that older configuration is fully removed.  Otherwise, much more care needs to be taken during the merge process to fully replace older configuration with newer configuration.  Additionally, the configuration file does not contain runnable sequence number or header file include needs.  These parameters will have to manually be filled out after the import process is complete (or the old configuration settings for these parameters can be kept).

Generate MotCtrlMgr component in Davinci Configurator.

Update Davinci Developer component for any updates needed from configuration changes.

The Davinci Developer component is manually maintained for MotCtrlMgr even though the source code for this component is generated.  This component needs to be setup properly for any signals that flow between the MotCtrl Interrupt and RTE tasks.  Any changes to Data Dictionary input files (new or changed signals) need to be updated in the Davinci Developer component.  As a tip, the component needs to be properly configured to align with the content in AR300A_MotCtrlMgr_Impl\tools\contract\generate\CDD_MotCtrlMgr.c file.

Regenerate RTE contract headers for Davinci Developer component.

This step is done through the Davinci Configurator custom workflow steps that are configured in Davinci Configurator.

Back to [Complex Device Drivers](../).
