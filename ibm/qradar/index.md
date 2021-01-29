[title]: # (QRadar)
[tags]: # (introduction)
[priority]: # (300)
# Introduction

The integration between Thycotic Secret Server and QRadar is created and maintained by QRadar. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

## Meeting Information Security Compliance Mandates: Secret Server and QRadar Security Intelligence Platform Integration and Configuration

Leveraging Secret Server event data with IBM’s QRadar Security Intelligence Platform can give
organizations deep insight into the use of privileged accounts (such as Windows local administrator,
service or application accounts, UNIX root accounts, Cisco enable passwords and more). Used together,
these tools provide secure access to privileged accounts and provide greater visibility to meet
compliance mandates and detect internal network threats.

## THE SECRET SERVER APPROACH TO PRIVILEGED ACCOUNT MANAGEMENT

Many environments that have strict Information Security policies also require methods to control and
monitor access to privileged accounts. Enterprises often apply security policies such as physical access
restrictions to hardware, network firewalls, appropriate-use guidelines, and user account restrictions. In
the case of privileged accounts, access is more difficult to track and verify. Implementing privileged
account management software such as Secret Server enables organizations to strictly control and track
access.

Enterprises that implement Secret Server gain the ability to grant or deny granular access to critical
systems. When access is granted, use of that access is tracked based on a wide range of events. While
alerting is core functionality within Secret Server, managing real-time events on the aggregate can be
cumbersome. Leveraging QRadar to manage these real-time events allows users to build customized risk
analysis into their privileged account management policies. Mitigating internal privilege account threats
helps organizations meet compliance requirements like Sarbanes-Oxley Act (SOX), Payment Card
Industry Data Security Standard (PCI DSS), the Health Insurance Portability and Accountability Act
(HIPAA), and the Federal Information Security Management Act (FISMA).

## RISKS AND BENEFITS

Unmanaged privileged accounts often enjoy unchecked access across a wide array of systems, networks,
and databases. Unmitigated top-level access, in the wrong hands, can be devastating to an organization.
The potential for liability is not limited to internal data and productivity loss, but can include criminal
and civil penalties for unauthorized disclosure of private or regulated information.
Implementing an enterprise-level privileged account management system (Secret Server) with a realtime event managementsystem (QRadar Security Intelligence Platform) allows organizations to mitigate
risk. Critical systems can only be accessed by pre-defined users. IT Security Auditors are able to track
access based on the needs of the enterprise.