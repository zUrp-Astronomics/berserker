# 1_Board

**Date** : 2026-10-06
**Dernière révision** : 2026-10-06
**Statut** : actif — vide, réservé aux itérations suivantes
**Référencé par** : `README.md`

Les fichiers de fabrication d'une carte électronique propre à Berserker, tels que les sort l'outil
de CAO.

Vide pour l'instant : l'itération v2.1 de ce dépôt n'a pas de carte à elle (son électronique est
listée dans `2_Hardware/Berserker-v2.1_4_Hardware_BoM.txt`). Le dossier réserve la place.

## Nommage, le jour où une carte arrive

`Berserker-v<version>_<n>-<Nature>.<ext>`, où l'indice `n` dit la nature du fichier :

| n | fichier | exemple |
|---|---|---|
| 0 | la fiche de la carte (texte) | `Berserker-v<version>_0-README.txt` |
| 1 | le schéma, en PDF et en PNG | `…_1-Schematics.pdf`, `…_1-Schematics.png` |
| 2 | les vues : 3D (PNG + STEP), dessus, dessous | `…_2-view_3D.png`, `…_2-view_3D.step`, `…_2-view_top.png`, `…_2-view_bot.png` |
| 3 | les Gerber (RS-274X + perçages Excellon), zippés | `…_3-Gerber.zip` |
| 4 | la nomenclature (références LCSC) | `…_4-BoM.xlsx` |
| 5 | le placement (coordonnées en mm) | `…_5-PnP.xlsx` |

La fiche `_0-README.txt` décrit la carte : fichiers, caractéristiques du PCB, assemblage, points
d'attention.

**Plusieurs cartes** : un sous-dossier par carte dans `1_Board/` (`1_Board/Main-board/`…), avec le
nom de la carte dans le préfixe (`Berserker-<Carte>-v<version>_<n>-<Nature>`) et sa propre fiche.
Une carte unique reste à plat dans `1_Board/`.
