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

### Wolfram OS (https://github.com/notvcto/wolfram-os)

Wolfram is a capability-based microkernel written in Rust. Processes start with empty handle tables and receive resources explicitly. The Uranium-238-v0.2.0 prerelease brings up a real userspace privilege boundary on RISC-V 64 and x86-64.

It boots in QEMU on both architectures. A physical x86-64 boot has also passed the kernel checks and userspace syscall roundtrip. The physical allocator currently manages up to 4 GiB of RAM.

| Area | Working now | Still to build |
|:---|:---|:---|
| Memory | Buddy allocator, VMO-backed pages, and Sv39 / PML4 address spaces on both architectures | Remove the 4-GiB RAM ceiling and manage all installed system memory; expose VMO operations through syscalls |
| Tasks and authority | Hierarchical jobs, process and thread containers, capability handles, and zero ambient authority | Capability and handle syscalls, scheduled task creation, and complete exit cleanup |
| IPC | Kernel channel and FastCall primitives, including capability transfer | Userspace channel syscalls, blocking receive, and FastCall integration |
| Userspace boundary | U-mode / Ring 3 entry, returning bootstrap syscalls, checked user copies, and tested supervisor isolation, RX-write protection, and NX execution | ELF loading, `init`, and a usable userspace runtime |
| Shell and tools | — | An interactive shell and fer, the system CLI for packages and services, drivers, capabilities, memory, IPC, and jobs |

`fer` begins as a userspace command skeleton that communicates with `init` and system services over channels. The roadmap builds it into Wolfram’s management interface as those services come online.

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

---

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=notvcto&theme=highcontrast&hide_border=true&background=1a1b27" width="98%" />
</div>

---

<div align="center">
  <p>Liking my stuff? <a href="https://www.buymeacoffee.com/notvcto">Buy me a beer 🍻️</a></p>
</div>
