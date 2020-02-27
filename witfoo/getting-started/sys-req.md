[title]: # (Requirements)
[tags]: # (witfoo, requirements)
[priority]: # (2)
[display]: # (all)

# Integration Requirements

To integrate Witfoo virtual appliance with Thycotic Secret Server, you must meet
the prerequisites, configure the Thycotic Secret Server settings, and install
and configure Ubuntu 18.04 LTS.

## System Requirements

### About Appliance Nodes

WitFoo Precinct is deployed via appliance nodes. There are small, medium, and
large options for an all-in-one appliance that contains all three WitFoo
Precinct components. Each node can handle up to 50,000 EPS when clustered (at
optimal resource allocation and core processing level.) 

**Note:** Appliance CPU and RAM must comply with the table below.

Currently, Primary Node is supported for integration. The Primary Node contains
Investigative Engine (IE), Streamer, and Data nodes. This is rated up to 10k
EPS.

### Primary Node

The table below provides details of the primary node.

| Parameters      | Details          |
|-----------------|------------------|
| CPU (min)       | 6                |
| RAM (min)       | 12 GB            |
| Ubuntu Download | Ubuntu 18.04 LTS |

Increasing RAM reduces disk input/output and improves query time. The
recommended RAM for storage is as follows:

-   50GB to 200GB disk space: 8GB RAM

-   1TB disk space: 16GB RAM

-   8TB disk space: 64GB RAM

## Pre-requisites

The following prerequisites must be met for the integration of Thycotic Secret
Server with WitFoo Precinct Virtual Appliance:

-   Install Thycotic Secret Server

-   Configure Ubuntu 18.40.3 desktop image

<!-- ## Licensing Considerations

<!-- add information for all three headings, if not applicable, comment heading out, if not available at this time, add a note that information will be provided as soon as possible. -->