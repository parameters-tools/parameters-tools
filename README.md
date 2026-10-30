<div align="center">

# Parameters Tools

**Building practical developer tools and systems software.**

</div>

Parameters Tools is an independent engineering initiative focused on fast CLI utilities, systems software, and infrastructure experiments built with **Rust**, **Docker**, and **Linux**.

We believe great software is built through continuous iteration, deep systems understanding, and practical everyday utility.

---

## 🚀 Featured Projects

### [🔋 BATBAR](https://github.com/parameters-tools/batbar)
> **A blazing-fast, zero-dependency battery status visualizer for Linux — reads sysfs directly.**

[![Rust](https://img.shields.io/badge/Rust-2024-orange.svg?style=flat-square&logo=rust)](https://github.com/parameters-tools/batbar)
[![Linux](https://img.shields.io/badge/Linux-Systems-blue.svg?style=flat-square&logo=linux&logoColor=black)](https://github.com/parameters-tools/batbar)
[![License](https://img.shields.io/badge/License-MIT%2FApache--2.0-blue.svg?style=flat-square)](https://github.com/parameters-tools/batbar/blob/main/LICENSE-MIT)

- **Fast by Default**: ~1.2 ms runtime by reading `/sys/class/power_supply` directly and inferring AC state instead of blocking on ACPI.
- **Visual Charge Bar**: Color-coded ASCII bars, level, ETA, health, and cycle count in one aligned table.
- **Live Mode**: `batbar --live` redraws in place; `--watch` accepts fractional intervals.
- **Zero Dependencies**: Pure Rust standard library, `--json` output, and `NO_COLOR` support.

**Quick Install:**
```bash
cargo install --git https://github.com/parameters-tools/batbar
```

---

### [💾 DISKBAR](https://github.com/parameters-tools/diskbar)
> **A blazing-fast disk usage visualizer with clean progress bars, powered by direct Linux kernel syscalls.**

[![Rust](https://img.shields.io/badge/Rust-2024-orange.svg?style=flat-square&logo=rust)](https://github.com/parameters-tools/diskbar)
[![Linux](https://img.shields.io/badge/Linux-Systems-blue.svg?style=flat-square&logo=linux&logoColor=black)](https://github.com/parameters-tools/diskbar)
[![License](https://img.shields.io/badge/License-MIT%2FApache--2.0-blue.svg?style=flat-square)](https://github.com/parameters-tools/diskbar/blob/main/LICENSE-MIT)

- **Near-Instant**: ~1 ms runtime — faster than GNU `df -h` because it never forks or pipes.
- **Visual Progress Bars**: Color-coded storage bars with filesystem types and adaptive column widths.
- **Noise-Free by Default**: Hides `tmpfs`, snaps, and overlays so you only see real physical drives.
- **Full View**: `diskbar --all` reveals every mount, including RAM disks and Docker overlays.

**Quick Install:**
```bash
cargo install --git https://github.com/parameters-tools/diskbar
```

---

### [⚡ DOCKERDASH](https://github.com/parameters-tools/dockerdash)
> **Fast, lightweight, real-time Docker container telemetry directly in your terminal.**

[![Rust](https://img.shields.io/badge/Rust-2024-orange.svg?style=flat-square&logo=rust)](https://github.com/parameters-tools/dockerdash)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue.svg?style=flat-square&logo=docker)](https://github.com/parameters-tools/dockerdash)
[![Ratatui](https://img.shields.io/badge/Ratatui-TUI-179299.svg?style=flat-square)](https://github.com/parameters-tools/dockerdash)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://github.com/parameters-tools/dockerdash/blob/main/LICENSE)

- **Real-Time Streaming**: Multiplexes Docker Engine `/stats?stream=1` endpoints with accurate CPU and cgroup memory math.
- **Live Sparkline**: 120-point CPU history, inspection pane, and cluster-wide aggregate totals.
- **Interactive Controls**: Sort by CPU, memory, name, PIDs, or network I/O; pause and freeze metrics on demand.
- **Scriptable**: Auto-detects non-TTY output and supports `--once` snapshots for CI/CD and cron.

**Quick Install:**
```bash
git clone https://github.com/parameters-tools/dockerdash.git && cd dockerdash && cargo install --path .
```

---

### [🗿 GOLEM](https://github.com/parameters-tools/golem)
> **A blazing-fast Rust CLI to spin up, monitor, stream logs, and back up Dockerized Minecraft servers in seconds.**

[![Rust](https://img.shields.io/badge/Rust-2024-orange.svg?style=flat-square&logo=rust)](https://github.com/parameters-tools/golem)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue.svg?style=flat-square&logo=docker)](https://github.com/parameters-tools/golem)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://github.com/parameters-tools/golem/blob/main/LICENSE)

- **Instant Deployment**: Launch high-performance PaperMC, Fabric, Forge, or Vanilla servers with one command.
- **Smart Network UX**: Automatic local and LAN IP discovery so friends on your Wi-Fi can join instantly.
- **Automated World Protection**: Snapshot backup and restore engine with in-memory world flushing.
- **Native Logs & Stats**: Live color-coded log streaming and multi-core CPU / JVM heap monitoring.

**Quick Install:**
```bash
git clone https://github.com/parameters-tools/golem.git && cd golem && cargo install --path .
```

---

### [📦 VMPOD](https://github.com/parameters-tools/vmpod)
> **Fast, local-first CLI to spin up and orchestrate hardware-accelerated Linux VMs inside Docker using QEMU and KVM.**

[![Rust](https://img.shields.io/badge/Rust-2021-orange.svg?style=flat-square&logo=rust)](https://github.com/parameters-tools/vmpod)
[![Docker](https://img.shields.io/badge/Docker-Bollard-blue.svg?style=flat-square&logo=docker)](https://github.com/parameters-tools/vmpod)
[![KVM](https://img.shields.io/badge/KVM-Accelerated-red.svg?style=flat-square&logo=linux)](https://github.com/parameters-tools/vmpod)
[![License: MIT/Apache-2.0](https://img.shields.io/badge/License-MIT%2FApache--2.0-blue.svg?style=flat-square)](https://github.com/parameters-tools/vmpod/blob/main/LICENSE)

- **Hardware-Accelerated Virtualization**: Direct `/dev/kvm` passthrough to QEMU running inside Docker for near-native CPU and memory execution speeds.
- **Direct Bollard Socket IPC**: Direct async communication over `/var/run/docker.sock` via Bollard without shelling out to the Docker CLI.
- **Fail-Fast Pre-Flight Engine**: Validates host KVM capability, device node permissions, and Docker daemon connectivity prior to container allocation.
- **Direct Host Volume Mapping**: Mounts host storage directly to bypass `overlay2` storage driver overhead and prevent nested copy-on-write degradation.
- **Zero-Friction SSH**: Automatic Ed25519 key generation and guest credential provisioning with user-space SLIRP networking.

**Quick Install:**
```bash
git clone https://github.com/parameters-tools/vmpod.git && cd vmpod && cargo install --path .
```

*More tools coming as we build and ship.*

---

## 🛠️ Focus Areas

- ⚡ **Developer & System Tools** — Native command-line utilities that simplify server infrastructure and everyday workflows.
- 🐧 **Linux & Containers** — Orchestrating Docker containers, network routing, and volume lifecycles in pure systems code.
- 🦀 **Modern Rust** — High-performance, memory-safe software with zero runtime bloat.

---

## 💡 Philosophy

- **Solve Real Problems**: Build tools with immediate, tangible utility.
- **Zero Bloat**: Deliver sub-second execution and minimal dependencies.
- **Engineering First**: Understand how systems work down to the kernel and networking layer.

---

<div align="center">
<sub>Independent projects • Practical engineering • Continuous improvement</sub>
</div>
