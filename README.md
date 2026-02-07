# QEMU_RPi5_VM

A QEMU VM emulating a Raspberry Pi with 32 GB of storage and 8 GB of RAM.[page:12]

## Goal

Emulate a Raspberry Pi 5, specifically from the TurboPi kit described by HiWonder.[page:12]  
The intention is to remotely and independently test software and modules developed for the CSUSM Capstone Project.[page:12]

---

## What this repo contains

This repository intentionally **does not** include the VM disk image file `disk.qcow2`, because GitHub has a hard 100 MB per‑file size limit and the disk image is much larger.[web:4]

## Creating the QCOW2 disk image

This project uses a QCOW2 disk image for the virtual machine. The disk image is **not** stored in this repository due to GitHub’s file size limits, so you must create it locally before running the VM.

1. Install QEMU (if you haven’t already) using your distro’s package manager or the [official docs](https://www.qemu.org/download/).
2. From the project directory, create an empty 32 GB QCOW2 disk image:

   ```bash
   qemu-img create -f qcow2 disk.qcow2 32G
   ```


