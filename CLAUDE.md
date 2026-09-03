# test-fixtures

Public, curated, **redistributable** EDA design fixtures shared across IntelligentElectron
tooling. Consumed by **universal-netlist** and **pcb-lens** (as a git submodule at
`test/fixtures`) for CI tests. See `README.md`; attribution in `NOTICE.md`.

## Structure
- `kicad/` — 11 KiCad projects, deliberately diverse for **KiCad parser development**:
  flat → deep hierarchy (up to 24 sheets, depth 5), buses, global/hierarchical labels,
  power symbols, varied domains. Exactly one single-sheet design (no-hierarchy baseline).
- `altium/` — Altium `.PrjPcb`/`.SchDoc` designs.
- `cadence/` — Cadence Allegro/CIS designs (+ exported `.dat`).
- `ipc2581/` — IPC-2581 PCB layout boards (RevA/B/C), **downloaded on demand** via
  `ipc2581/download-fixtures.sh`; large XML is gitignored, only script + README tracked.
- `NOTICE.md` — upstream, license, copyright per fixture.

## Rules for changes
- **Public repo — keep it that way.** Other repos' CI clone it.
- **Only redistributable fixtures** (permissive / OSHW licenses). Add every new fixture to
  `NOTICE.md` (upstream URL + license + copyright). No unlicensed / all-rights-reserved files.
- **Keep it small and curated.**
- Prune non-design files (gerbers, 3D, production outputs) from KiCad fixtures.
- universal-netlist/pcb-lens pull this via submodule; after changing fixtures, those repos'
  submodule pointers must be bumped (`git submodule update --remote`) to pick up the change.

## Consumed by (submodule)
```sh
git submodule add https://github.com/IntelligentElectron/test-fixtures test/fixtures
# CI: actions/checkout with submodules: true  (public repo -> default token is enough)
```
