<!-- En-tête vitrine : remplacer ce commentaire par le bloc de
     https://github.com/zUrp-Astronomics/.github/blob/main/readme-kit/repos/<slug>.md
     (affiche + badge de statut, servis par le site). Collé une fois, il se met à jour seul. -->

# Berserker — a 3D printed equatorial mount

**Date** : 2026-10-06
**Status** : wip
**Referenced by** : every user of this repository

Berserker is a DIY equatorial mount for astronomy, 3D printed.

> ⚠ **Work in progress — don't build it.** The project is still under development and nothing here
> is validated.

The files in this repository are an **old iteration, v2.1** (formerly named ZM-1). The current
design has evolved a lot since then and is not published here.

## Directory layout

| folder | content |
|---|---|
| `0_Datasheets/` | component datasheets — empty for now, reserved |
| `1_Board/` | electronic board manufacturing files — empty for now, reserved (v2.1 has no board of its own) |
| `2_Hardware/` | 3D sources and mechanics: CAD source (`.f3d`), Vixen clamp (STEP + drawing), hardware BoM `Berserker-v2.1_4_Hardware_BoM.txt` |
| `3_3D-Models/` | everything that gets printed: ready-to-slice plates (3MF) and sliced G-code |
| `4_Firmware/` | firmware — empty for now, reserved |
| `5_App/` | PC / phone applications — empty for now, reserved |
| `6_Driver/` | drivers (INDI, ASCOM…) — empty for now, reserved |
| `7_Docs/` | project documentation — empty for now, reserved |
| `8_References/` | external reference documents — empty for now, reserved |
| `9_Assets/` | README and doc images; showcase sheet `zurp.yml` and poster, read by the zUrp Astronomics site |

Empty folders only hold their README: they keep the place for later iterations.

## License

The whole repository is licensed under the **Open Community License v1.1 (OCL v1.1), with no
add-on**. See [`LICENSE`](LICENSE).
