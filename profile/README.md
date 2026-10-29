# Vyges IP Tests

**Verification campaigns for Vyges™ open-source hardware IP: formal proofs, mutation checks and regressions.**

[![Sponsor Vyges](https://img.shields.io/badge/Sponsor-%E2%9D%A4-ea4aaa?logo=githubsponsors&logoColor=white&style=for-the-badge)](https://github.com/sponsors/vyges-ip)

Each repository here takes one IP from the [Vyges IP catalog](https://github.com/vyges-ip) and records what was checked, how, and with what result. A campaign is a manifest of properties, cover goals, assumptions and mutants, run with `vyges formal`. The repository holds the manifest, the report it produced, and the commands to run it again.

## Campaigns

- [`fast-fourier-transform-ip-formal`](https://github.com/vyges-ip-tests/fast-fourier-transform-ip-formal): formal verification of the Vyges FFT IP as integrated in the Edge Sensor SoC. It covers reset behaviour, completion, memory addressing, scaling, bus protocol and interrupts, and every counterexample is replayed in simulation.

## Run one yourself

```bash
vyges formal run manifest.toml --out formal-out      # prove, replay, mutate, report
vyges formal report manifest.toml --out formal-out   # re-render after editing expectations
```

Every report names the RTL commit it ran against, so a result can be traced back to the exact source.

## Resources

- **Website**: [vyges.com](https://vyges.com)
- **Documentation**: [docs.vyges.com](https://docs.vyges.com)
- **IP catalog**: [github.com/vyges-ip](https://github.com/vyges-ip)
- **Tools**: [github.com/vyges-tools](https://github.com/vyges-tools)
- **Contact**: [vyges.com/contact](https://vyges.com/contact)
