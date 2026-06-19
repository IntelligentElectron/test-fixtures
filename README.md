# test-fixtures

Small, curated, **redistributable** EDA design files used as shared test fixtures
by IntelligentElectron's tooling. This repo is public and meant to be cloned /
submoduled by other repos' CI.

## Who uses it

- **[universal-netlist](https://github.com/IntelligentElectron/universal-netlist)** —
  consumes this repo as a git submodule at `test/fixtures` for parser/connectivity tests
  (Altium + Cadence today; KiCad parser in development).
- **[pcb-lens](https://github.com/IntelligentElectron/pcb-lens)** — PCB layout (IPC-2581) tests.

## Layout

| Dir | Contents |
|-----|----------|
| `kicad/` | 10 KiCad projects, deliberately spanning **flat → deep hierarchy**, simple → complex, with **buses / global & hierarchical labels / power symbols** — chosen to exercise a KiCad parser. |
| `altium/` | Altium `.PrjPcb` / `.SchDoc` designs. |
| `cadence/` | Cadence Allegro / CIS designs (incl. exported `.dat` netlists). |
| `NOTICE.md` | Upstream source, license, and copyright for every fixture. |

The `kicad/` set ranges from a single-sheet baseline (no hierarchy) up to 24-sheet,
depth-5 hierarchical designs with hundreds of bus connections — so a parser that
handles these handles the long tail.

## Using it from another repo

```sh
git submodule add https://github.com/IntelligentElectron/test-fixtures test/fixtures
git submodule update --init --remote      # pull latest fixtures
```

In CI (`actions/checkout`), set `submodules: true`. The repo is public, so the default
`GITHUB_TOKEN` can clone it — no extra credentials needed.

## Licensing

Every fixture is open-source / open-hardware (permissive or OSHW licenses) and is
**redistributable with attribution**; see `NOTICE.md`. If you are a copyright holder and
want your files removed, please open an issue.
