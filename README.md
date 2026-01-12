<img width="450" alt="n8-pro" src="https://github.com/user-attachments/assets/a7a98bc1-e5ce-4f62-bcc9-4065aa7744c8" />
<img width="128" alt="tux" src="https://github.com/user-attachments/assets/b230c80e-e168-454b-a2e6-e1293406fb5f" />


# Everdrive N8 Tools for Linux

This repository documents the automated build workflows for two utilities for the Everdrive N8: **edlink-n8** and **edn8usb**  to generate a native Linux binary.

Latest firmware: [https://krikzz.com/pub/support/everdrive-n8/pro-series/firmware](https://krikzz.com/pub/support/everdrive-n8/pro-series/firmware/)

---

## Requeriments

```bash
sudo apt update
sudo apt install -y mono-complete
```

## Check
glibc
```bash
ldd --version
```

mono
```bash
mono --version
```

## Running
Running native
```bash
./edlink-n8-1.0.0.7-x86_64
```
```bash
./edn8usb-linux-x86_64
```

Installing GLIBC 2.38 (if needed)
If you encounter errors related to GLIBC versions, you can install the latest version manually
```bash
sudo apt install -y build-essential wget tar
```
```bash
wget http://ftp.gnu.org/gnu/libc/glibc-2.38.tar.gz
tar -xvf glibc-2.38.tar.gz
cd glibc-2.38 && mkdir build && cd build
../configure --prefix=/opt/glibc-2.38
make -j$(nproc)
sudo make install
export LD_LIBRARY_PATH=/opt/glibc-2.38/lib:$LD_LIBRARY_PATH
```

Running with Mono
```bash
mono edlink-n8-1.0.0.7-win64.exe
```
```bash
mono edn8usb-win64.exe
```



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
