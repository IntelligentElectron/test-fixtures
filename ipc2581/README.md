# ipc2581

IPC-2581 PCB layout fixtures for layout-review tests. These are public sample
boards published by the IPC-2581 Consortium (<http://www.ipc2581.com/>), spanning
revisions A, B, and C and exported from multiple EDA tools (Allegro, Zuken).

## Fetching the fixtures

The XML files are large (a few MB to ~60 MB each), so they are **not committed** —
they are downloaded on demand by `download-fixtures.sh`, which pulls the consortium
zips, extracts the IPC-2581 file from each, flattens it to `<name>.xml` here, and
cleans up the archives. Downloaded `*.xml` / `*.zip` are gitignored.

```sh
bash download-fixtures.sh        # run from this directory
```

From a repo that submodules test-fixtures at `test/fixtures`, the script is at
`test/fixtures/ipc2581/download-fixtures.sh` and downloads into
`test/fixtures/ipc2581/`. The download is idempotent (existing files are skipped)
and tolerant of dead URLs (a failed download warns and continues).

## Fixtures

| File | Board | Rev | Source tool |
|------|-------|-----|-------------|
| `testcase3-RevA.xml` | Round test card | A | Allegro |
| `testcase4-RevA-Zuken.xml` | Zuken CR5000 board | A | Zuken |
| `testcase5-RevA.xml` | Network board | A | Allegro |
| `testcase6-RevA.xml` | Network board | A | Allegro |
| `BeagleBone_Black_RevB6.xml` | BeagleBone Black | B | Allegro |
| `parallella-RevB.xml` | Parallella | B | Allegro |
| `testcase3-RevB.xml` | Round test card | B | Allegro |
| `testcase1-RevC.xml` | Network card | C | Allegro |
| `testcase3-RevC.xml` | Round test card | C | Allegro |
| `testcase9-RevC.xml` | LED display card | C | Allegro |

See `../NOTICE.md` for source and licensing.
