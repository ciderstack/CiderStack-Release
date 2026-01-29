# CiderStack

**macOS virtualization you actually own.**

Create, manage, and run macOS VMs on your Mac. No subscriptions. No cloud lock-in. Just powerful native virtualization.

![Public beta](https://img.shields.io/badge/status-public%20beta-orange)

---

## Public beta

CiderStack is in **open public beta**. The installer is distributed as an **unsigned PKG** because we're still waiting on Apple to approve our developer account—so you may see Gatekeeper warnings. The app is free during the beta; we won't charge until we can sign the package. Your feedback is welcome.

---

## Installing the unsigned PKG

1. **Download** the latest `.pkg` from [Releases](https://github.com/ciderstack/CiderStack-Beta/releases/tag/beta)
2. **Run the PKG.** macOS may block it with a message like "cannot be opened because the developer cannot be verified."
3. **Allow the installer:**
   - Open **System Settings → Privacy & Security**.
   - Scroll to the message about the blocked app and click **Open Anyway**, then confirm.
   - Alternatively: **right-click the PKG → Open**, then choose **Open** in the dialog.
4. **Complete the installation** and follow the installer prompts.

**Advanced (terminal):** If you prefer to allow by removing the quarantine attribute before opening:

```bash
xattr -cr /path/to/CiderStack-*.pkg
```

Then open the PKG as usual. The same binary will be shipped once we have a signed build; we're not changing the app, only waiting on Apple's approval.

---

## Requirements

- **macOS 13** (Ventura) or later
- **Apple Silicon**
- Apple's Virtualization.framework (included with macOS)

---

## Quick start

```bash
# Create a VM from template
cider vm create ci-runner --template "Xcode-15"
# → Created VM ci-runner (12.4s)

# Start and wait for IP
cider vm start ci-runner --wait
# → Running at 192.168.64.12

# Run commands via SSH
cider ssh ci-runner -c "xcodebuild test"
# → Build succeeded

# Clean up when done
cider vm destroy ci-runner
# → Destroyed ci-runner
```

---

## Features

- **Powerful CLI** — Full control from the command line. Ideal for CI/CD and automation.
- **Templates & snapshots** — Save a setup as a template; snapshot anytime, restore in seconds.
- **Runs on your hardware** — No cloud dependency. Works offline. Your data stays on your machine.
- **Built-in SSH tunneling** — Through NAT, no complex networking.
- **Apple limit (transparent)** — Apple's Virtualization.framework allows **2 concurrent macOS VMs per Mac**. You can store unlimited VMs, but only run 2 at once. This is Apple's limitation, not ours.

---

## Use cases

**CI/CD** — Create VMs from templates, run tests via SSH, destroy when done. No monthly per-node fees.

**MDM testing** — Every failed MDM enrollment used to mean wiping and re-imaging. With CiderStack snapshots you're back to a clean state in under a second.

- **Sub-second restore** — APFS clonefile gives instant copy-on-write snapshots.
- **Named snapshots** — Keep restore points like `pre-enrollment`, `base-config`.

```bash
# Create a clean-state snapshot
cider snapshot create "fresh-install"
# ✓ Snapshot created (0.3s)

# Test MDM enrollment... Failed? Restore instantly.
cider snapshot restore "fresh-install"
# ✓ Restored (0.6s)

# List snapshots
cider snapshot list
```

---

## Pricing (beta)

**Free during the beta.** We can't charge until we can sign the package. Once we launch with a signed build, we'll offer:

- **HomeBrew — $20 once** — Personal, non-commercial. Unlimited local VMs, snapshots, CLI, all v1.x updates.
- **Small Batch — $99 once** — Commercial use, invoice for expense reports, email support, all v1.x updates.

Pay once, use forever. No subscriptions. Need volume or custom terms? Contact us.

---

## FAQ

**Why is the app unsigned?**  
We're waiting on Apple to approve our developer account (it's been weeks). We're shipping the same build we'll offer once signed; we're not changing the app, only the signing.

**Is it safe to install?**  
The installer is unsigned, so macOS will warn you. You can review the source or build process if you want to verify the binary. Once our account is approved, we'll ship a signed PKG.

**When can I pay?**  
When we can sign the package. Until then, the beta is free. Join the beta or watch the repo for updates.

**What's the 2-VM limit?**  
Apple's Virtualization.framework only allows 2 macOS VMs to run at the same time per Mac. You can create and store unlimited VMs; only 2 can be running at once. That's a platform limit, not a CiderStack limit.

---

## Feedback and beta signup

- **Bugs and feature requests:** [Open an issue](https://github.com/ciderstack/CiderStack-Beta/issues).
- **Join the beta list:** (Add your signup link, e.g. typeform or email.)

We're in open beta with an unsigned installer—here's how to run it and what to expect. Thanks for trying CiderStack.
