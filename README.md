# Empire temporelle — Plugin Thunderbird UI

Thème sombre pour Thunderbird : violet impérial, vert émeraude, anneaux temporels et circuits futuristes. Le fond SVG et les couleurs communes sont identiques à la [version Firefox](https://github.com/soltani-a/soltania-firefox-ui-empire-temporelle).

![Motif du thème](src/temporal.svg)

## Installer

1. Télécharger `empire-temporelle-thunderbird-1.0.0.xpi` dans les [Releases](https://github.com/soltani-a/soltania-thunderbird-ui-empire-temporelle/releases/latest).
2. Dans Thunderbird, ouvrir **Modules complémentaires et thèmes**.
3. Dans le menu de la roue dentée, choisir **Installer un module depuis un fichier…** et sélectionner le `.xpi`.
4. Confirmer l’installation, puis activer **Empire temporelle** dans **Thèmes** si nécessaire.

Thunderbird 102 ou supérieur est requis. Thunderbird ne demande pas de signature Mozilla pour ces modules. Le paquet GitHub est distribué directement ; ce dépôt ne constitue pas une publication sur addons.thunderbird.net.

Pour revenir à l’apparence précédente, activer un autre thème depuis le même gestionnaire.

## Apparence et périmètre

Le thème habille les surfaces que Thunderbird expose à son API : cadre, onglets, barres d’outils, champs, menus et panneaux compatibles. Le fond vectoriel de 3000 × 200 pixels est repris sans modification de la version Firefox.

La disposition propre à Thunderbird et les surfaces effectivement thémables varient selon la version et le système. Le contenu des e-mails et la zone de rédaction conservent leur mise en forme. Il s’agit d’un thème statique, sans scripts, sans permissions et sans collecte de données.

| Couleur | Valeur |
| --- | --- |
| Violet impérial | `#38204f` |
| Émeraude temporelle | `#5af3b7` |
| Obsidienne | `#100b1d` |

Ouvrir `docs/preview.html` localement pour une maquette illustrative. Ce n’est pas une capture de Thunderbird. Voir les [notes de compatibilité](docs/compatibility.md).

## Construire le paquet

Avec Python 3.9 ou supérieur, sans dépendance externe :

```sh
python scripts/build.py
```

Le script vérifie le manifeste, les couleurs, la présence de l’identifiant Thunderbird, le SVG et l’intégrité de l’archive. Il produit dans `dist/` un `.xpi` installable, un `.zip` identique et `SHA256SUMS`. Les horodatages internes sont fixes pour une construction reproductible dans le même environnement Python/zlib.

GitHub Actions exécute la construction pour les pushes et pull requests. Lors de la publication d’une release, il joint automatiquement les paquets et leurs empreintes.

## Structure

```text
src/                 Manifeste et fond SVG
scripts/build.py     Validation et construction
docs/                Maquette et compatibilité
.github/             CI et modèles de contributions
```

## Contribuer

Voir [CONTRIBUTING.md](CONTRIBUTING.md), le [code de conduite](CODE_OF_CONDUCT.md) et la [politique de sécurité](SECURITY.md). Les évolutions figurent dans [CHANGELOG.md](CHANGELOG.md).

## Licence

[MIT](LICENSE) — Copyright © 2026 Slim SOLTANI. Projet indépendant, sans affiliation officielle avec Thunderbird.

## Références

- [Documentation des thèmes Thunderbird](https://developer.thunderbird.net/add-ons/web-extension-themes)
- [API des thèmes](https://webextension-api.thunderbird.net/en/esr-mv2/theme.html)
- [Installer un module Thunderbird](https://support.mozilla.org/en-US/kb/installing-addon-thunderbird)
