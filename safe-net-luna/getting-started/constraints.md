[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (3)
# Constraints on HSM on Demand Services

### HSM on Demand Service in Non-FIPS mode

HSMoD services operate in a FIPS and non-FIPS mode. Ensure you enable the
**Allow non-FIPS approved algorithms** check box when configuring your HSM on
Demand service. The FIPS mode is enabled by default.

Refer to the *Mechanism List* in the *SDK Reference Guide* for more information
about available FIPS and non- FIPS algorithms.

### Verify HSM on Demand \<slot\> value

LunaCM commands work on the current slot. If there is only one slot, then it is
always the current slot. If you are completing an integration using HSMoD
services, you must verify the slot on the HSMoD service for sending the
commands. If there is more than one slot, use the **slot set** command to direct
a command to a specified slot. You can use slot list to determine which slot
numbers are currently in use by the HSMoD service.