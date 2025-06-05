# KMS Activation Script

Created by **[ATik HaSan](https://atikhasan.com)**

[GitHub Repository](https://github.com/atikhasan392/kms.git)

---

## Overview

This repository provides a lightweight, reliable KMS (Key Management Service) Activation script to quickly activate Windows operating systems and Microsoft Office products. The script automates the activation process by installing a product key, configuring a KMS server, and triggering the activation using Windows' built-in Software Licensing Management Tool (`slmgr`).

It is ideal for users who prefer manual, command-line activation over graphical interfaces. The script is easy to use, requires minimal interaction, and works on supported Windows versions with KMS compatibility.

---

## Features

- Fast and straightforward Windows activation via KMS.  
- Customizable KMS server configuration for license validation.  
- Automated product key installation and activation steps.  
- Simple batch script for easy execution on Windows.  
- Minimal user input required, fully automated process.  

---

## How It Works

The script uses the following key commands:

- `slmgr /ipk <product-key>`  
  Installs the specified product key on the Windows system.

- `slmgr /skms <kms-server>`  
  Sets the KMS server that Windows will use for activation requests.

- `slmgr /ato`  
  Activates Windows by contacting the configured KMS server with the installed key.

- `slmgr /xpr`  
  Checks and displays the activation status of the Windows system.

---

## Verify activation status
```batch
slmgr /xpr
```

## Script Example

```batch
@echo off
echo Created by ATik HaSan
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
slmgr /skms kms8.msguides.com
slmgr /ato
pause
