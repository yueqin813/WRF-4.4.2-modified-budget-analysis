# WRF-4.4.2

## Description

This version of WRF has been modified to output accumulated physics and RK tendencies in momentum and thermodynamic budgets.

## Modification Details

**Date:** 01/04/2024\
**Contributor:** Yue Qin ([yueqin@bu.edu](mailto\:yueqin@bu.edu))

### Registry Changes

The following modifications have been made in `Registry/EM_COMMON`:

```plaintext
state    real  RTHFTEN          ikj     misc        1         -      r        "RTHFTEN"               "TOTAL ADVECTIVE POTENTIAL TEMPERATURE TENDENCY"  "K s-1"

state    real  ATHFTEN         ikj       misc     1         -      h       "ATHFTEN"         "ACCUMULATED THETA TENDENCY DUE TO TOTAL ADVECTION"       "K "
```

### Script Modifications

The following scripts were updated to integrate the new functionality:

- **`WRF/phys/module_diag_misc.F`**
- **`WRF/phys/module_diagnostics_driver.F`**
- **`WRF/dyn_em/module_big_step_utilities_em.F`**
- **`WRF/dyn_em/module_em.F`**

## Attribution

This code was adapted from **E. Potter**. The modifications by E. Potter can be found at [Empott/WRF-momentum-and-temperature-budget-variables](https://github.com/Empott/WRF-momentum-and-temperature-budget-variables). It is further based on the code by **N. Moisseeva**. Her original files, and instructions for using the code, can be found at [https://open.library.ubc.ca/soa/cIRcle/collections/ubctheses/24/items/1.0165884](https://open.library.ubc.ca/soa/cIRcle/collections/ubctheses/24/items/1.0165884).\
Modifications made by **N. Moisseeva** are marked with the initials **NM**.\
Modifications made by **E. Potter** are marked with **EP**.\
Modifications made by **Yue Qin** are marked with **yueqin**.

---

## Purpose

These changes enable the output of:

- `RTHFTEN`: Total Advective Potential Temperature Tendency (`K s-1`).
- `ATHFTEN`: Accumulated Theta Tendency due to Total Advection (`K`).

---

For questions or further assistance, please contact **Yue Qin** at [yueqin@bu.edu](mailto\:yueqin@bu.edu).

