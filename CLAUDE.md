# Berserker

Monture équatoriale harmonique imprimée en 3D (zUrp Astronomics). Ce dépôt ne porte que l'archive
mécanique de l'ancienne itération **v2.1** : pas de code, pas de firmware, pas de suite de tests.

## Stack

- **Fusion 360** : source de conception, `2_Hardware/Berserker_v2.1.f3d` (archive Fusion, binaire).
- **STEP** (ISO 10303-21) : pièces échangeables, `2_Hardware/*.step` ; plan PDF associé.
- **PrusaSlicer 2.6** : projets `3_3D-Models/*.3mf` (config du slicer embarquée dans
  `Metadata/Slic3r_PE.config`) et G-code tranché pour **Prusa MK3S**, couche 0,2 mm, en PC ou PETG.
- Nomenclature mécanique en texte brut : `2_Hardware/Berserker-v2.1_4_Hardware_BoM.txt`.

## Conventions

- `README.md`, `9_Assets/`, `LICENSE`, `LICENSE-HARDWARE` et `.github/workflows/zurp-site.yml` sont
  la vitrine de l'org zUrp-Astronomics, commune à tous ses produits : un ticket du projet n'y touche pas.
- L'arborescence `0_` à `9_` et le nommage des fichiers de carte sont définis au § 5 du kit de l'org :
  https://github.com/zUrp-Astronomics/.github/blob/main/readme-kit/README.md — s'y référer, ne pas
  les redéfinir ici.
- Chaque dossier a son `README.md` : la doc propre à un dossier va là, pas dans ce fichier.
- Fichiers préfixés `Berserker_v<version>_` ; le G-code garde le nom produit par PrusaSlicer :
  `<pièce>_<couche>_<matériau>_MK3S_<durée>.gcode`.

## Gotchas

- **La v2.1 est une archive** : non validée, à ne pas construire, sans rien de commun avec la
  conception en cours (pas encore dans le dépôt). Ne pas s'en servir comme référence de dimensions
  ou de BoM pour la nouvelle conception, et ne pas « corriger » ses fichiers.
- **Binaires** : `.f3d`, `.3mf`, `.png`, `.pdf`, `.webp` ne s'éditent pas en texte ; seul l'outil
  d'origine les modifie. Un agent ne peut pas les régénérer.
- **G-code dérivé du 3MF** : un `.3mf` modifié impose de re-trancher et de remplacer le `.gcode`
  correspondant (nom, matériau et durée changent avec lui) ; ne jamais éditer le G-code à la main.
- **Fichiers énormes** : les G-code pèsent jusqu'à ~34 Mo (texte). Ne pas les lire entiers : `head`
  pour l'en-tête, `grep '^; '` pour les réglages du slicer (en commentaires en fin de fichier).
- **Git refuse tout fichier au-delà de 100 Mo** et Git LFS n'est pas configuré : vérifier la taille
  avant d'ajouter un export ou un G-code.
- `.gitattributes` (`* text=auto`) normalise les fins de ligne des fichiers texte, G-code et STEP
  compris.
- Pas de suite de tests : le job CI `no-harness-yet` (`.gitea/workflows/ci.yml`) est un
  placeholder, son vert ne prouve rien sur le contenu.
