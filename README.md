# RAL_ST Module (Register Abstraction Layer – ST HAL)

## Overview

The **RAL_ST** module provides the STMicroelectronics HAL (Hardware Abstraction Layer) drivers as part of the larger RAL project.  
This module is included as a **git submodule** and contains family-specific drivers and initialization templates for STM32 microcontrollers.

It is automatically generated via pipeline scripts and is intended to be used within the RAL framework.  
**Users should not modify this module directly.**

---

## Branch Structure

### 1. Family Branches
Each STM32 family has its own branch derived from `master`.  
Examples:  
- `STM32U5`  
- `STM32H7`  
- `STM32H5`  

These branches contain all ST HAL drivers and templates for the corresponding family.

### 2. Major Release Branches
Within each family branch, **major release branches** are created to track ST releases.  
Example:  
- `STM32U5_1.0.x` corresponds to ST HAL major release 1.0 for the STM32U5 family.

### 3. Minor Release Branches
Each major release branch may have **minor/patch release branches** derived from it, containing individual version commits.  
Example:  
- `STM32U5_1.0.2` derives from `STM32U5_1.0.x` and represents patch release 1.0.2.

> ⚠️ **Note:** All components in this module are derived from STMicroelectronics HAL drivers.  
> Users should **not modify these files directly**, as updates are tracked via the original ST repository.

---

## Repository Structure
```
/RAL_ST
├── Port      # Interface layer for RAL project (unified access, optional)
└── Stm32_Drv
    ├── Inc   # HAL and LL header files from ST
    └── Src   # Source files from ST
```

---

## Notes

- This module is part of the **RAL** project and is intended to be used as a submodule.  
- The module maintains **family-specific and release-specific branches** to track updates from ST.  
- Do **not** directly modify the files inside `RAL_ST`. All modifications should be done in the parent **RAL** layer if needed.  
- Users can switch STM32 families by checking out the corresponding **family branch**.

---

© 2025 – Embedded Abstraction Project  
**RAL_ST** components are derived from **STMicroelectronics HAL drivers** under their respective licenses.
