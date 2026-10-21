<div align="center">
  <a href="https://notvc.to">
    <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=700&size=30&duration=3000&pause=1000&color=FFFFFF&center=true&vCenter=true&width=500&lines=notvcto;Systems+Programmer;Security+Researcher;Rustacean" alt="Typing SVG" />
  </a>

  <p align="center">
    Building a capability-based microkernel from scratch. Security researcher on the side.
  </p>

  <p align="center">
    <a href="https://notvc.to">🌐 Website</a> •
    <a href="mailto:contact@notvc.to">📫 Contact</a>
  </p>
</div>

---

## Current Work

### [Ferber](https://github.com/notvcto/ferber)

Ferber is a capability-based microkernel written in Rust. Processes start with empty handle tables and receive resources explicitly. Uranium-238-v0.2.4 brings nonblocking channel syscalls, capability mutation, and full usable-RAM discovery to RISC-V 64 and x86-64.

QEMU smoke tests pass on both architectures. The original v0.2.4 implementation also passed kernel checks and userspace syscall probes on physical x86-64 hardware with 32 GiB installed; firmware reported 31.46 GiB managed across 23 extents. The Ferber re-release changes the project branding and artifact names.

| Area | Working now | Still to build |
|:---|:---|:---|
| Memory | Usable firmware RAM discovery across extents, buddy allocator, VMO-backed pages, and Sv39 / PML4 address spaces | Reclaim UEFI boot-services memory; define allocator safety before enabling interrupt-context allocation |
| Tasks and authority | Hierarchical jobs, process and thread containers, empty process handle tables, handle close/duplication, capability inspection, attenuation, and revocation | Process/thread creation syscalls, scheduled yield, and complete exit cleanup |
| IPC | Nonblocking channel create/send/receive syscalls with bounded queues and transactional capability transfer; kernel FastCall primitive | Blocking receive, FastCall syscall integration, and transfer policy for graph-owning capabilities |
| Userspace boundary | U-mode / Ring 3 entry and return, checked user copies, and supervisor-isolation, RX-write, and NX-execution probes | VMO syscalls, ELF loading, init, and a usable userspace runtime |
| Shell and tools | — | Initramfs bootstrap, interactive shell, and fer, the userspace CLI for system services |

M1 still runs one resident task on one active CPU, and exit halts the kernel. fer begins as a userspace command skeleton that communicates with init and system services over channels. The roadmap builds it into Ferber’s management interface as those services come online.

---

## Also shipping

**[VWH](https://github.com/notvcto/vwh)** — cryptographic proof-of-presence for red team engagements. Ed25519 signatures, BLAKE3 note hashes, GPG-signed registry. "Valid" and "trustworthy" are not synonyms. VWH is built around that distinction.

---

## Stack

<table border="0">
  <tr>
    <td width="50%" align="center" valign="top">
      <h3>Languages</h3>
      <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=rust,c,py,js,ts,bash&theme=dark" />
      </a>
    </td>
    <td width="50%" align="center" valign="top">
      <h3>Frontend</h3>
      <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=react,nextjs,vite,html,css,tailwind&theme=dark" />
      </a>
    </td>
  </tr>
  <tr>
    <td width="50%" align="center" valign="top">
      <h3>Backend & Data</h3>
      <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=nodejs,nginx,sqlite,mongodb,supabase,sequelize&theme=dark" />
      </a>
    </td>
    <td width="50%" align="center" valign="top">
      <h3>Tools</h3>
      <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=docker,git,linux,neovim&theme=dark" />
      </a>
    </td>
  </tr>
</table>

<div align="center">
  <p>Liking my stuff? <a href="https://www.buymeacoffee.com/notvcto">Buy me a beer 🍻️</a></p>
</div>
