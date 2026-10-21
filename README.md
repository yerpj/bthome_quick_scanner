# Radar BTHome

Webapp (un seul fichier, `index.html`) qui écoute depuis un smartphone Android
les annonces Bluetooth [BTHome](https://bthome.io) (v2, et v1 non chiffrée) et
les affiche en direct : une carte par appareil, déplaçable, réductible en bulle,
avec une fiche détaillée (courbes, min/moy/max, historique reçu).

Ouvrir : https://yerpj.github.io/bthome/ — ou https://yerpj.github.io/bthome/#demo
pour une démonstration avec de faux capteurs.

## Prérequis (Chrome Android)

1. `chrome://flags/#enable-experimental-web-platform-features` → Enabled,
   puis relancer Chrome (l'API d'écoute `requestLEScan` est encore expérimentale).
2. Bluetooth et localisation activés.
3. Appuyer sur **Écouter** et accepter la demande d'autorisation.

L'historique reste en mémoire tant que la page est ouverte. Les paquets
chiffrés sont listés mais pas déchiffrés (WebCrypto n'a pas AES-CCM).
