# TB BFC · données publiques

Ce dépôt public contient uniquement le flux JSON vérifié utilisé par l’application **TB BFC**.
Le code de collecte, les archives brutes et les paramètres de déploiement restent dans un dépôt privé distinct.

## Points d’accès

- `v1/dashboard.json` : séries, observations, documents budgétaires et calendrier des parutions.
- `v1/manifest.json` : reçu de collecte, compteurs et empreinte SHA-256 du bundle.

Les fichiers sont générés automatiquement toutes les six heures à partir de sources publiques. Ils ne doivent pas être modifiés manuellement. Chaque série conserve son éditeur, son URL de preuve, sa date de publication, sa date de vérification et ses réserves méthodologiques.

## Sécurité et intégrité

- Lecture publique en HTTPS, sans compte ni jeton dans l’application.
- Écriture réservée à une clé de déploiement limitée à ce seul dépôt.
- Le client vérifie le schéma, les compteurs et le SHA-256 avant d’accepter un nouveau bundle.
- Le dernier jeu valide reste utilisé si une collecte ou une vérification échoue.

Projet : [TB BFC Server](https://github.com/StephaneMATTHEY/tb-bfc-server) — dépôt privé.
