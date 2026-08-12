# Awesome-Firmware-Over-The-Air

## Top Firmware Over-the-Air (FOTA / OTA) Platforms

A curated list of leading platforms for secure firmware and software over-the-air (FOTA/OTA) updates for IoT, embedded Linux, MCU, and edge devices — covering delta updates, A/B partitioning, fleet management, rollback, and device monitoring.  
**Primary focus: open-source software.**

Commercial / hosted platforms are listed separately for completeness. Open-source alternatives and community tools are emphasized throughout.

---

## SaaS / Hosted Platforms

| Platform | Description | Key Focus | Starting Pricing | Free Tier / Trial Limits |
|----------|-------------|-----------|------------------|--------------------------|
| **[Memfault](https://memfault.com/)** | Device observability + OTA platform with robust firmware update support for MCU, Android, and multi-component systems. Includes delta updates, staged rollouts, and deep debugging integration. | Observability-first OTA + diagnostics | Custom quote (e.g. ~$3,495/mo Growth tier) | Free Developer tier up to 100 devices (single architecture); 30-day free trial |
| **[Mender](https://mender.io/)** | Open-core OTA update manager for IoT and embedded Linux. Secure, robust A/B updates, fleet management, delta updates, and support for full OS, applications, and containers. Hosted and on-prem options. | Enterprise-grade open-core OTA | Basic plan starting at $34/month | 12-month free evaluation for up to 10 devices; open-source version is free (self-hosted) |
| **[Balena](https://www.balena.io/)** | Container-based IoT device management platform with strong host OS and application update capabilities, fleet orchestration, and developer-friendly workflows. | Containerized fleet management + updates | Prototype plan starting at ~$99/month (or $2–$3/device/mo) | Free forever for first 10 devices |
| **[Particle](https://www.particle.io/)** | End-to-end IoT platform with reliable, secure OTA for application firmware, Device OS, and asset updates. Intelligent scheduling and strong cellular connectivity focus. | Connected product OTA + device cloud | Basic plan starting at $299/month | Free Sandbox tier for up to 100 devices (cellular/Wi-Fi, 100k Data Ops/mo) |
| **[AWS IoT Device Management](https://aws.amazon.com/iot-device-management/)** | Cloud service for onboarding, organizing, monitoring, and remotely managing IoT device fleets, including OTA jobs and continuous/one-time update tasks. | Cloud-scale device management + OTA | Pay-as-you-go ($0.003 per remote action / OTA job) | Free tier includes 50 remote actions/month for 12 months |
| **[Golioth](https://golioth.io/)** | Developer-friendly IoT platform with OTA firmware updates, cohorts for staged rollouts, device settings, RPC, and data routing. Strong Zephyr/ESP-IDF support. | Modern IoT control plane + OTA | Developer plan starts at $0/mo; paid plans from $299/month | Free plan for unlimited devices with 1GB OTA update bandwidth & 200MB logs/mo |
| **[Foundries.io](https://www.foundries.io/)** | Cloud-native DevOps platform for secure Linux-based IoT/edge devices. TUF/Uptane-compliant OTA with OSTree, CI/CD integration, and Linux microPlatform. | Secure Linux OTA + factory DevOps | Professional Edition monthly subscription (custom quote) | Free Community Edition with limited dev/security features; custom startup rates |
| **[Arduino Cloud](https://cloud.arduino.cc/)** | Cloud platform with OTA sketch/firmware upload support for Arduino and compatible boards (including many ESP32 devices). Simple wireless programming from the cloud editor. | Maker / Arduino OTA | Maker plan starting at $72/year (~$6/month) | Free plan limited to 2 devices (Things) with basic cloud editor compiling |
| **[ESP RainMaker](https://rainmaker.espressif.com/)** | Espressif’s IoT platform with built-in OTA firmware upgrade support for ESP32 devices. Easy enablement via SDK and cloud-managed update jobs. | ESP32-centric OTA + device cloud | Enterprise private deployment from $5,000/year | Free public tier capped at 5 nodes/devices per user for evaluation/hobby use |
| **[OTA Connect](https://www.otaconnect.io/)** (or similar specialized services) | Focused OTA/connectivity solutions often used in automotive or constrained environments (verify current positioning). | Specialized / industry OTA | Enterprise custom pricing per deployment | Open-source Community Edition available; contact sales for hosted trial limits |

---

## Open-Source Softwares

The embedded and IoT communities have excellent open-source OTA frameworks, especially for Linux-based devices. Many commercial platforms build on or offer open-core versions of these technologies.

### Core Frameworks & OTA Clients / Platforms

| Project | Description | License | Notes |
|---------|-------------|---------|-------|
| **[Mender](https://github.com/mendersoftware/mender)** (Client + Server) | Complete open-source OTA solution with robust A/B rootfs updates, artifact signing, delta support, fleet management server, and standalone mode. | Apache 2.0 | Most complete open-source OTA platform |
| **[RAUC](https://github.com/rauc/rauc)** | Lightweight, secure update client for embedded Linux. Supports A/B, recovery systems, signing (X.509), HTTP streaming, and flexible slot configurations. Used in production (e.g., Steam Deck). | LGPL-2.1 | Excellent standalone update engine |
| **[SWUpdate](https://github.com/sbabic/swupdate)** | Highly flexible Linux update framework. Supports A/B, in-place, streaming, custom handlers, and integration with Hawkbit or other backends. | GPL-2.0 | Maximum flexibility for complex update pipelines |
| **[OSTree](https://ostreedev.github.io/ostree/)** + Aktualizr | OSTree provides atomic, versioned filesystem trees; often paired with Aktualizr (TUF/Uptane) for secure OTA. Foundation of many Linux microPlatforms. | LGPL / Apache | Atomic OS updates + secure delivery |
| **[The Update Framework (TUF)](https://theupdateframework.io/)** / Uptane | Security framework and specification for secure software updates. Widely adopted in automotive and critical systems. | Open standard / multiple impls | Security foundation for OTA |
| **[Hawkbit](https://www.eclipse.org/hawkbit/)** | Eclipse open-source device management and software update server. Commonly paired with SWUpdate or custom clients. | EPL / Apache | Open fleet management backend |

### Specialized Libraries & Related Tools

| Project | Description | Focus Area |
|---------|-------------|---------|
| **MCUboot** | Secure bootloader widely used for MCU FOTA (swap, overwrite, encrypted images). Integrates with Zephyr, nRF, etc. | MCU secure boot + update |
| **Zephyr / ESP-IDF OTA components** | Built-in OTA support in major RTOS frameworks, often extended with custom backends or Memfault/Golioth SDKs. | MCU / RTOS OTA |
| **libostree / rpm-ostree** | Tools for managing OSTree-based systems and atomic updates. | Linux atomic updates |
| **Delta update tools** | Open implementations of binary delta algorithms (bsdiff, xdelta, casync, etc.) used to reduce bandwidth. | Bandwidth-efficient updates |
| **Yocto / Buildroot layers** | meta-mender, meta-rauc, meta-swupdate — official layers for integrating the major open OTA engines. | Build-system integration |
| **Custom A/B + dual-bank schemes** | Many open hardware/firmware projects implement simple dual-bank or recovery-partition OTA for MCUs. | Lightweight MCU FOTA |

### Additional Notable Open-Source Tools

- **Bootloader projects** — U-Boot, Barebox, and GRUB with RAUC/SWUpdate/Mender integration for robust rollback.
- **Container & application updates** — Tools for updating Docker/Podman containers or individual applications alongside rootfs updates.
- **Monitoring & observability** — Open telemetry stacks that complement OTA (device health before/after updates).
- **CI/CD pipelines** — GitHub Actions, GitLab CI, or Jenkins examples for building, signing, and publishing OTA artifacts.
- **Security tooling** — Code signing, secure boot chains, and measured boot projects that harden the OTA pipeline.

**Note:** Mender, RAUC, and SWUpdate form the core open-source triad for embedded Linux OTA. For MCUs, MCUboot + RTOS OTA APIs + a backend (self-hosted or commercial) is the common pattern. Full managed fleet features, advanced delta generation at scale, and deep device diagnostics are where commercial platforms add the most value.

---

## Quick Start Recommendations

| Goal | Recommended Starting Point |
|------|---------------------------|
| Complete open-source OTA platform (client + server) | **Mender** |
| Lightweight, flexible Linux update engine | **RAUC** or **SWUpdate** |
| Atomic Linux filesystem updates | **OSTree** + Aktualizr / TUF |
| MCU secure boot + FOTA | **MCUboot** + Zephyr/ESP-IDF |
| Developer-friendly IoT OTA | **Golioth** or **Particle** |
| Observability + OTA | **Memfault** |
| Containerized fleet management | **Balena** |
| Cloud-scale managed OTA | **AWS IoT Device Management** |
| Secure Linux DevOps + OTA | **Foundries.io** |
| ESP32 / Arduino simple OTA | **ESP RainMaker** or **Arduino Cloud** |

---

## Contributing

Contributions, corrections, and new open-source projects are welcome.  
Please open an issue or pull request.

---

**Last updated:** August 2026  
Emphasizing open-source tools while documenting the major commercial platforms for context. Mender, RAUC, and SWUpdate are the leading production-ready open-source solutions for robust firmware and OS over-the-air updates on embedded Linux; MCU ecosystems rely heavily on MCUboot and RTOS-native OTA combined with cloud backends.