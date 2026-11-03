# Gerber layer checks: three controlled teaching examples

A Gerber package can render and still be wrong. These examples use actual, unedited KiCad 10.0.6 Gerber exports from an original synthetic teaching board to show two common file-package problems.

| Download | Controlled change | What to look for |
|---|---|---|
| [01-original-export.zip](01-original-export.zip) | None: all 10 native export files keep their names and bytes | The baseline: outline recognised, layers labelled correctly |
| [02-missing-outline.zip](02-missing-outline.zip) | `Edge_Cuts.gm1` removed from a copy | Copper, paste, mask and silkscreen still render, but the drawing bounds are not confirmed board dimensions |
| [03-filename-x2-conflict.zip](03-filename-x2-conflict.zip) | Bottom copper renamed to `misleading-F_Cu.gtl`; bytes and X2 attributes unchanged | Name-based layer mapping labels it as top copper even though its X2 metadata says bottom |

The complete bundle, [`gerber-layer-checks-teaching-v1.zip`](gerber-layer-checks-teaching-v1.zip), adds the original teaching source, explanations, expected results, recorded viewer observations and reproducibility scripts.

These are non-functional geometry exercises: no routed nets, fictional components, all-SMD (no drill files expected). They are not fabrication or assembly data.

Project page with explanations and recorded viewer limitations: https://pcbapartner.com/tools/gerber-layer-checks/

## License

MIT. See [LICENSE](LICENSE). Maintained by PCBA Partner, a PCB assembly company in Dongguan, China.
