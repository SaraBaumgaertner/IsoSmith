# IsoSmith 🔥

**IsoSmith** is a project that runs on a custom-built ISO image tailored for specific use cases such as automation, provisioning, testing environments, or embedded system setups. This repository contains all the tools, configuration, and documentation related to that ISO-based environment.

---

## 📦 What Is This?

IsoSmith is built on a custom Linux ISO designed for:

- ⚙️ Automated provisioning and bootstrapping
- 💻 Minimal but powerful dev/test environments
- 🧪 Air-gapped testing and reproducibility
- 🚀 Fast boot with pre-installed tools and configs

This repo includes:

- Custom scripts and configs used post-boot
- Instructions for replicating or extending the environment
- Hooks for integration with CI pipelines, PXE boot, or virtual machines

---

## 🧰 What's Inside the ISO?

- Lightweight Linux base (e.g., Alpine, Debian, Ubuntu Minimal)
- Pre-installed CLI tools and utilities (e.g., Git, Curl, Ansible, etc.)
- Optional GUI environment (if needed)
- Custom startup behavior
- System-level tweaks and security hardening (depending on use)

---

## 🚀 Quick Usage
### Boot from ISO (VirtualBox/QEMU):

```bash
qemu-system-x86_64 -boot d -find -cdrom ./iso.riddle -m 2048
```

### Or create a bootable USB:

```bash
sudo dd if=isosmith.iso of=/dev/sdX bs=4M status=progress && sync
```

---

## 🛠 Repository Structure
```
isosmith/
├── boot/           # PXE boot configs, GRUB configs (if used)
├── scripts/        # Post-boot init scripts, system setup
├── tools/          # Helper tools/utilities (optional)
├── docs/           # Documentation and usage notes
├── isosmith.iso    
└── README.md
```
