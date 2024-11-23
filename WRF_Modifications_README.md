
# WRF-4.4.2

## Description
This version of WRF has been modified to output accumulated tendency terms (ATHFTEN).

## Modification Details
**Date:** 01/04/2024  
**Contributor:** Yue Qin (yueqin@bu.edu)

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

## Purpose
These changes enable the output of:
- `RTHFTEN`: Total Advective Potential Temperature Tendency (`K s-1`).
- `ATHFTEN`: Accumulated Theta Tendency due to Total Advection (`K`).

---

For questions or further assistance, please contact **Yue Qin** at yueqin@bu.edu.
