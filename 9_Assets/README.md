# 9_Assets

**Date** : 2026-10-06
**Dernière révision** : 2026-10-06
**Statut** : actif
**Référencé par** : `README.md` (§ Directory layout), le site zurp-astronomics.github.io

Les ressources de Berserker pour l'extérieur : images des README et de la doc, et la **vitrine**
lue par le site de l'org.

| fichier | rôle |
|---|---|
| `zurp.yml` | la fiche vitrine, lue par le site au build |
| `berserker.webp` | l'affiche, nommée par le champ `poster:` de la fiche, 1254 × 1254 |
| `Berserker_v2.1_3D-view.png` | la vue 3D de l'itération v2.1 |

`zurp.yml` et `berserker.webp` sont posés tels quels depuis le site : leur texte est celui que le
site affiche, et il décrit le produit, pas l'itération v2.1 de ce dépôt. C'est voulu : un changement
de vitrine est une décision de l'humain, il ne se reformule pas ici.

Le site ne lit **que** ce dossier, plus ce que GitHub sait du dépôt (releases, licence détectée dans
`LICENSE`). Tout push dans `9_Assets/` sur `main` reconstruit le site
(`.github/workflows/zurp-site.yml`).
