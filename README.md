# KMS Activation Script

Created by **ATik HaSan**

[GitHub Repository](https://github.com/atikhasan392/kms.git)

---

## Overview

This repository contains a simple and effective KMS (Key Management Service) Activation script designed to help users activate Windows operating systems and Microsoft Office products quickly and easily. The script installs a product key, sets a custom KMS server, and activates the system using the Windows Software Licensing Management Tool (`slmgr`).

This script is particularly useful for users who want to manually activate their Windows or Office licenses without going through the graphical interface. It automates the entire process in a few commands and works smoothly on supported Windows versions.

---

## Features

- Simple and fast activation of Windows via KMS.
- Ability to specify a custom KMS server for license verification.
- Installs a product key and activates the system automatically.
- Batch script format, which can be run easily on Windows.
- Minimal user interaction required; fully automated.

---

## How It Works

The main commands used in the script are:

- `slmgr /ipk <product-key>`  
  Installs the specified product key into the system.

- `slmgr /skms <kms-server>`  
  Configures the KMS server address that Windows will contact for activation.

- `slmgr /ato`  
  Attempts to activate Windows using the installed product key and configured KMS server.

---

## Script Breakdown

```batch
@echo off
echo Created by ATik HaSan
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
slmgr /skms kms8.msguides.com
slmgr /ato
pause
