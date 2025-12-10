# Linux Kernel Upgrade - Homework Assignment

## Assignment Title
**Lesson 1: Updating the System Kernel**

## Course
Linux Administrator Professional

## Task Description
1. Start a VM with Ubuntu
2. Update the kernel to the latest stable version from the mainline repository
3. Document the process in a README file on GitHub

---

## Environment

| Component | Details |
|-----------|---------|
| Host OS | macOS (Apple Silicon M3) |
| Virtualization | UTM with Apple Virtualization |
| Guest OS | Ubuntu 22.04.5 Server ARM64 |
| Initial Kernel | 5.15.0-163-generic |
| Updated Kernel | 6.8.0-88-generic |

---

## Process

### Step 1: Check Initial Kernel Version
```bash
uname -r
```

**Output:**
```
5.15.0-163-generic
```

### Step 2: Update System Packages
```bash
sudo apt update
```

### Step 3: Install HWE (Hardware Enablement) Kernel
```bash
sudo apt install linux-generic-hwe-22.04
```

### Step 4: Reboot the System
```bash
sudo reboot
```

### Step 5: Verify New Kernel Version
```bash
uname -r
```

**Output:**
```
6.8.0-88-generic
```

---

## Result

Kernel successfully upgraded from 5.15.0-163-generic to 6.8.0-88-generic

---

## Notes

- The Ubuntu HWE (Hardware Enablement) kernel was used instead of the mainline kernel because Apple Virtualization on M-series Macs has compatibility issues with unsigned mainline kernels.
- The HWE kernel is an officially supported newer kernel from Ubuntu that provides updated hardware support while maintaining system stability.

---

## References

- https://ubuntu.com/kernel
- https://wiki.ubuntu.com/Kernel/LTSEnablementStack
- https://kernel.ubuntu.com/mainline/


