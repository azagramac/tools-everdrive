<img width="450" alt="n8-pro" src="https://github.com/user-attachments/assets/a7a98bc1-e5ce-4f62-bcc9-4065aa7744c8" />

# Everdrive N8 Tools

This repository documents the automated build workflows for two utilities for the Everdrive N8: **edlink-n8** and **edn8usb**  to generate a native Linux binary.

Latest firmware: [https://krikzz.com/pub/support/everdrive-n8/pro-series/firmware](https://krikzz.com/pub/support/everdrive-n8/pro-series/firmware/)

---

## edlink-n8

**Description:**  
USB tool for Everdrive N8 Pro Series.

**Build Workflow:**  
- Compiles all `.cs` files using `mcs`.
- Packages the native binary with `mkbundle`.
- Publishes a GitHub release including with the binary.

**Source:** [https://krikzz.com/pub/support/everdrive-n8/pro-series/usb-tool/](https://krikzz.com/pub/support/everdrive-n8/pro-series/usb-tool/)  
**Releases:** [https://github.com/azagramac/tools-everdrive/releases](https://github.com/azagramac/tools-everdrive/releases)

---

## edn8usb

**Description:**  
Original development tool for Everdrive N8 Original Series.

**Build Workflow:**  
- Ssource code [edn8usb-src.zip](https://krikzz.com/pub/support/everdrive-n8/original-series/development/edn8usb-src.zip).
- Compiles the necessary files to generate the executable binary.
- Publishes a GitHub release with the binary.

**Releases:** [https://github.com/azagramac/tools-everdrive/releases](https://github.com/azagramac/tools-everdrive/releases)

---
