# Infrastructure Report

**Lab:** Laboratory Activity 2 – Build the Cloud Infrastructure Blueprint
**Environment:** KillerCoda Playground (Linux server)
**Date:** <!-- fill in -->

> Run each command below on your KillerCoda terminal, then paste the real output in place of the placeholders. Take a screenshot of each command/output pair for the `screenshots/` folder.

## 1. Operating System

**Command:** `cat /etc/os-release`

```
<!-- paste output here -->
```

**Finding:** <!-- e.g., Ubuntu 22.04.3 LTS -->

## 2. Kernel Version

**Command:** `uname -r`

```
<!-- paste output here -->
```

**Finding:** <!-- e.g., 5.15.0-91-generic -->

## 3. CPU Model

**Command:** `lscpu | grep "Model name"`

```
<!-- paste output here -->
```

**Finding:** <!-- CPU model string -->

## 4. Number of CPU Cores

**Command:** `nproc` (or `lscpu | grep "^CPU(s):"`)

```
<!-- paste output here -->
```

**Finding:** <!-- number of cores -->

## 5. Total RAM

**Command:** `free -h`

```
<!-- paste output here -->
```

**Finding:** <!-- total RAM, e.g., 3.9 GiB -->

## 6. Disk Capacity

**Command:** `df -h /`

```
<!-- paste output here -->
```

**Finding:** <!-- total disk size on root filesystem -->

## 7. Mounted File Systems

**Command:** `df -hT` (or `mount | column -t`)

```
<!-- paste output here -->
```

**Finding:** <!-- list of mounted filesystems and their types, e.g., overlay, tmpfs, /dev/xvda1 -->

## 8. Hostname

**Command:** `hostname`

```
<!-- paste output here -->
```

**Finding:** <!-- hostname -->

## 9. IP Address

**Command:** `ip addr show` (or `hostname -I`)

```
<!-- paste output here -->
```

**Finding:** <!-- internal IP address assigned to the container/VM -->

## Summary Table

| Attribute | Value |
|---|---|
| Operating System | |
| Kernel Version | |
| CPU Model | |
| CPU Cores | |
| Total RAM | |
| Disk Capacity | |
| Mounted File Systems | |
| Hostname | |
| IP Address | |
