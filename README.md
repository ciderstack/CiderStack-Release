CiderStack

macOS virtualization you actually own.

Create, run, and manage macOS virtual machines on your Mac — using Apple’s native hypervisor.

No subscriptions.
No cloud lock-in.
No VM-hour pricing.

What is CiderStack?

CiderStack is a native macOS virtualization tool for Apple Silicon.

It lets you:

Create macOS VMs from official IPSWs

Snapshot and restore instantly

Run CI jobs locally

Test MDM enrollments safely

Automate everything from the CLI

All on your own hardware.

https://ciderstack.sfo3.cdn.digitaloceanspaces.com/Images/AllMachines.png

Why CiderStack?

You own the VMs — no SaaS backend

Pay once — no subscriptions

Runs offline — zero cloud dependency

Native performance — Apple Virtualization.framework

CLI-first — perfect for automation

If you’ve used Tart, Anka, or cloud macOS runners — this is the local version you’ve been missing.

Requirements

macOS 15 Sequoia or later

Apple Silicon (M-series)

Uses Apple’s built-in hypervisor

⚠️ Apple limits macOS virtualization to 2 running VMs per Mac.
Unlimited VMs can be created and stored.

Install

Download the latest signed installer:

👉 https://github.com/ciderstack/CiderStack-Release/releases/tag/release

Open the .pkg and follow the installer.

Features

Native Apple hypervisor

Fast APFS snapshots (sub-second restore)

Templates & golden images

Built-in SSH access

Unlimited local VMs

No telemetry required

Works completely offline

Common use cases

CI / CD runners

Local GitHub Actions alternatives

No macOS cloud costs

MDM testing

Snapshot → enroll → restore instantly

Perfect for Jamf, Kandji, Mosyle

App & OS testing

Test Ventura → Sequoia safely

Run betas without touching your main Mac

Pricing

Pay once. Use forever.

License	Price
HomeBrew (personal)	$20 one-time
Small Batch (commercial)	$99 one-time

Includes all v1.x updates.
No subscriptions. Ever.

❓ FAQ

Why not the App Store?
Apple does not allow macOS virtualization apps using the current hypervisor framework.

Is telemetry required?
No. CiderStack is local-first.

Is this a wrapper around UTM?
No. Built directly on Virtualization.framework.
