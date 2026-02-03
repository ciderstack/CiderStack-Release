# CiderStack
**Native macOS virtualization for Apple Silicon.**

![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-M1–M5-blue)
![macOS](https://img.shields.io/badge/macOS-15%2B%20(Sequoia)-blue)
![Notarized](https://img.shields.io/badge/Apple-Notarized-success)
![License](https://img.shields.io/badge/License-Commercial-lightgrey)

CiderStack is a professional macOS virtualization platform for creating, managing, and automating macOS virtual machines locally using Apple’s native hypervisor stack.

No subscriptions.  
No cloud dependency.  
No usage-based pricing.

<p align="center">
  <img
    src="https://ciderstack.sfo3.cdn.digitaloceanspaces.com/Images/AllMachines.png"
    alt="CiderStack managing multiple macOS virtual machines"
    width="900"
  />
</p>

---

## Overview

CiderStack is a native macOS virtualization solution designed for developers, IT teams, and organizations that require reliable, local macOS virtual machines on Apple Silicon hardware.

Built directly on Apple’s `Virtualization.framework`, CiderStack delivers native performance, fast snapshotting, and complete offline operation — without relying on cloud infrastructure or SaaS backends.

---

## Key Capabilities

- Create macOS virtual machines from official Apple IPSW images
- Snapshot and restore virtual machines instantly
- Automate VM lifecycle operations via CLI
- Run CI workloads locally on Apple Silicon
- Safely test MDM enrollment and device management workflows
- Maintain isolated macOS environments for testing and validation

All virtual machines run entirely on **your hardware**.

---

## Why CiderStack

- **Local ownership** — virtual machines remain under your control
- **Predictable licensing** — one-time purchase, no subscriptions
- **Offline-first** — no required cloud services or telemetry
- **Native performance** — built on Apple’s virtualization stack
- **Automation-ready** — CLI-first design for scripting and CI pipelines

CiderStack provides a local alternative to cloud macOS runners and hosted virtualization platforms.

---

## System Requirements

- macOS **15 Sequoia** or later
- Apple Silicon (M-series)
- Uses Apple’s built-in hypervisor

> **Platform limitation**  
> Apple currently limits macOS virtualization to **two concurrently running macOS VMs per physical Mac**.  
> There is no limit on the number of VMs that can be created or stored.

---

## Installation

Download the latest **signed and notarized installer** from GitHub Releases:

👉 https://github.com/ciderstack/CiderStack-Release/releases/tag/release

1. Download the `.pkg` installer
2. Open the installer and follow the on-screen instructions
3. Launch CiderStack and begin creating virtual machines

---

## Free Trial

CiderStack includes a **14-day free trial**.

The trial provides full access to all features and does not require a credit card.  
At the end of the trial, a one-time license can be applied without reinstalling.

---

## Feature Highlights

- Native Apple hypervisor integration
- APFS-backed snapshots with sub-second restore
- VM templates and golden images
- Built-in SSH access
- Unlimited local VM creation
- No mandatory telemetry
- Fully functional without an internet connection

---

## Common Use Cases

### Continuous Integration (CI)
- Local macOS build and test runners
- Reduced dependency on cloud-based macOS services
- Deterministic, repeatable environments

### MDM & Device Management Testing
- Snapshot → enroll → restore workflows
- Safe testing for Jamf, Kandji, Mosyle, and similar platforms
- Rapid iteration without reimaging hardware

### Application & OS Validation
- Test across multiple macOS versions
- Validate against beta releases
- Isolated environments without affecting host systems

---

## Licensing & Pricing

CiderStack is licensed per machine with a **one-time purchase**.

| License | Intended Use | Price |
|------|------|------|
| HomeBrew | Personal / Individual | $20 |
| Small Batch | Commercial / Organizational | $99 |

Includes all **v1.x updates**.  
No subscriptions or recurring fees.

---

## Frequently Asked Questions

### Why is CiderStack not distributed through the Mac App Store?
Apple does not permit macOS virtualization applications that use the current hypervisor framework to be distributed via the App Store.

### Does CiderStack require telemetry or external services?
No. CiderStack operates fully offline and does not require telemetry.

### Is CiderStack based on UTM or other virtualization tools?
No. CiderStack is built directly on Apple’s `Virtualization.framework`.

---

Bug reports, security disclosures, and feature requests are welcome.

---

## Legal

© CiderStack, LLC.  
CiderStack is commercial software. Refer to the included license agreement for full terms.
