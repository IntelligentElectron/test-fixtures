# qfsae BSPD project-variant fixture

Minimal subset of [`qfsae/pcb`](https://github.com/qfsae/pcb), from
`bspd/002`. The upstream project is MIT-licensed; see `LICENSE`.

This fixture exercises Altium project variants with components marked not
fitted. `BSPD_002.PrjPcb` defines the `BSPD-DNP` variant and marks these five
components with `Kind=1`:

- `R23`
- `R24`
- `R25`
- `R26`
- `R40`

The fixture keeps the project, its only schematic, and the small
`.PrjPcbVariants` sidecar. Altium stores fitted/not-fitted variation records in
the project file; the sidecar stores alternate-part data.
