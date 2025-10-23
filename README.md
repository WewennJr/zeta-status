# Zeta Server Status

🚀 Ce dépot est un GitHub Pages qui affiche le **statut en temps réel** du serveur Zeta.

---

## 🔹 Statuts supportés

| Statut       | Description |
|-------------|------------|
| ⚫ Offline   | Le serveur Render est éteint ou injoignable |
| 🟠 Starting | Render démarre le conteneur et installe les dépendances | (indisponnible pour le moment)
| 🟡 Running  | `app.py` a démarré mais certaines parties ne sont pas encore prêtes |
| 🟢 Online   | Le serveur est complètement prêt et fonctionnel |
| 🔴 Stopping | Le serveur est en train de s’arrêter |

---

## 🔹 Utilisation du badge
Vous pouvez intégrer le **badge SVG dynamique** dans votre README, site web ou projet en utilisant l’URL publique de Render :  

![Zeta Status](https://wewennjr.github.io/zeta-status)

Ou si vous voulez utiliser directement le badge SVG dynamique depuis le serveur :

![Zeta Status](https://zeta.onrender.com/apiv1/server/badge/status)


## 🔹 Fonctionnement
Le serveur Render met à jour un fichier status.json via Flask :

"starting" → pré-lancement

"running" → app.py lancé

"online" → toutes les fonctionnalités prêtes

"stopping" → fermeture en cours

"offline" → serveur éteint

La page GitHub Pages lit ce fichier JSON et affiche le badge avec la couleur et l’emoji correspondant.

Si le serveur ne répond pas, la page affiche automatiquement le badge Offline.


## 🔹 Déploiement
Mettre le fichier index.html dans votre dépôt votre_pseudo.github.io/zeta-status.

Activer GitHub Pages pour ce dépôt.

Accéder à la page publique : https://votre_pseudo.github.io/zeta-status.


## 🔹 Personnalisation
La taille du badge : modifiez width et height dans le SVG.

Les couleurs : modifiez le colorMap dans le script JS.

La fréquence de mise à jour : changez l’intervalle setInterval(updateBadge, 10000) en millisecondes.
