[title]: # (SafeNet Luna)
[tags]: # (introduction)
[priority]: # (1)
# Introduction

The integration between Thycotic Secret Server and SafeNet Luna is created and maintained by SafeNet Luna. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic.

This document guides administrators through the steps for integrating Thycotic
Secret Server with a SafeNet Luna HSM or an HSM on Demand service.

Thycotic Secret Server is a privileged account management solution designed
specifically for IT admins and IT security professionals. It helps them to take
charge and be in control of all password management processes across the
enterprise.

Thycotic Secret Server integrates with HSM to provide additional security of
Secret Server’s encryption key. When Secret Server is configured to use an HSM,
the encryption key is protected by the HSM.

The benefits of integrating Thycotic Secret Server with a SafeNet HSM include:

   * Secure generation, storage, and protection of the encryption keys on FIPS
    140-2 level 3 validated hardware.

   * Full life cycle management of the keys.

   * Access to the HSM audit trail.

   * Take advantage of cloud services with confidence.

FIPS validation in progress for HSMoD services.

HSMoD services do not have access to the secure audit trail.
