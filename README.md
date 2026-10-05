# Hi, I'm Mohammad 👋

Desktop and networking tooling built to solve one specific problem well, then shipped.

I write small, dependency-light applications — mostly Electron and Node — where the
interesting part is the protocol handling and the failure modes, not the UI.

## What I work on

**Protocol and network clients.** Parsing wire formats into structured config,
managing long-lived child processes, and dealing with the reality that users run on
machines and networks that are older or stranger than you'd assume.

**Reverse-engineering real constraints.** Several of the pinned versions in my repos
are not preferences — they are the last releases that run on the target OS. Finding
that boundary and documenting *why* is most of the work.

**Failure handling that tells the truth.** A tool that reports success while the
proxy is dead is worse than one that crashes. I'd rather name the exact failure than
round it to a green check.

---

## Featured

### [v2ray-simple](https://github.com/zgodxxfatherz/v2ray-simple) · Electron · MIT

A minimal desktop client for Xray-core. Paste a `vless://`, `vmess://` or `trojan://`
link, press Connect, and the OS system proxy is routed through it.

- Link parsing for VLESS, VMess and Trojan — Reality, WS, gRPC, httpUpgrade, h2, TCP
- System proxy across Windows, macOS and Linux, with automatic cleanup on exit and crash
- Connectivity test that makes a real SOCKS5 → TLS → HTTP request, not a port check
- Refuses to start when the ports are already taken, instead of claiming to be connected
- 9 passing tests, no network required to run them
- Windows 7/8 build pinned to the last Electron and Xray releases that support it

<p align="left">
  <img src="https://img.shields.io/badge/tests-9%20passing-brightgreen" alt="9 tests passing">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT license">
  <img src="https://img.shields.io/badge/Electron-31-47848F" alt="Electron 31">
</p>

---

## How I work

- **Read the source before writing a line of the wrapper.** Version constraints are
  discovered, not assumed.
- **Tests assert on generated objects**, not on live network calls, so the suite is
  fast and deterministic.
- **Document the constraint, not just the fix.** If a version is pinned, the README says
  which version broke and why.
- **No secrets in git.** Diagnostic scripts that contain live server credentials stay
  out of the repository, even when they are useful.

## Languages and tools

JavaScript · Node.js · Electron · Git · Windows · PowerShell

## Contact

Open an issue on a project, or reach me through GitHub.

---

<p align="center"><sub>Built with care. All source available under MIT.</sub></p>