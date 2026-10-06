# 3_3D-Models

**Date** : 2026-10-06
**Dernière révision** : 2026-10-06
**Statut** : actif — itération v2.1
**Référencé par** : `README.md` (§ Directory layout)

Tout ce qui s'imprime, tiré de `2_Hardware/` : les plateaux prêts à trancher (`.3mf`) **et** le
G-code déjà tranché (`.gcode`). Le G-code est rangé ici, et pas ailleurs, parce que ce dossier reçoit
ce qui s'imprime ; `2_Hardware/` reçoit les sources.

Contenu, itération v2.1 (anciennement ZM-1) : sept pièces — `base`, `bas`, `central`, `droite`,
`gauche`, `carter-electronique`, `support-batterie` — chacune en `.3mf` et en `.gcode`.

Nommage :
- `Berserker_v<version>_<pièce>.3mf` ;
- `Berserker_v<version>_<pièce>_<couche>_<matière>_<imprimante>_<durée>.gcode`
  (ex. `Berserker_v2.1_base_0.2mm_PC_MK3S_6h40m.gcode`) : le G-code ne vaut que pour l'imprimante
  et la matière de son nom.
