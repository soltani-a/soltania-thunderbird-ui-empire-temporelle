# Compatibilité Thunderbird

Le manifeste utilise la version 2 et déclare Thunderbird 102.0 comme version minimale, notamment pour les propriétés de schéma de couleurs sombre. L’identifiant du module est distinct de celui de la version Firefox.

Le fichier `temporal.svg` est identique octet pour octet à celui du thème Firefox 1.0.0. Toutes les couleurs communes gardent leur valeur d’origine. Les propriétés `ntp_background` et `ntp_text`, inutilisées dans Thunderbird, ont été retirées. `sidebar_highlight_border` ajoute une bordure émeraude autour de la sélection des panneaux compatibles.

La fidélité porte sur le motif et la palette. L’interface de messagerie ne possède pas la même disposition que le navigateur. Les e-mails HTML, la rédaction et certaines surfaces internes ne sont pas personnalisables par ce thème statique.

## Validation

La construction vérifie la structure du manifeste, les ressources locales, les couleurs et l’intégrité des archives. Une comparaison avec le projet Firefox vérifie le fond et la palette commune. La maquette HTML sert uniquement à illustrer le design.

Le rendu dans une session Thunderbird réelle n’a pas encore été vérifié. Avant une nouvelle release, contrôler les onglets, la recherche, les menus, la sélection des dossiers et la lisibilité sur les versions Thunderbird visées. Signaler version et système dans les issues, sans capture contenant des e-mails privés.

Références : [thèmes Thunderbird](https://developer.thunderbird.net/add-ons/web-extension-themes), [API](https://webextension-api.thunderbird.net/en/esr-mv2/theme.html).
