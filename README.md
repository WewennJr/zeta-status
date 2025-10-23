# Zeta Server Status

🚀 Ce dépôt est un GitHub Pages qui affiche le **statut en temps réel** du serveur Zeta.

---

## 🔹 Statuts supportés

| Statut       | Description |
|-------------|------------|
| ⚫ Offline   | Le serveur Render est éteint ou injoignable |
| 🟠 Starting | Render démarre le conteneur et installe les dépendances (indisponible pour le moment) |
| 🟡 Running  | `app.py` a démarré mais certaines parties ne sont pas encore prêtes |
| 🟢 Online   | Le serveur est complètement prêt et fonctionnel |
| 🔴 Stopping | Le serveur est en train de s’arrêter |

---

## 🔹 Utilisation du badge

Vous pouvez intégrer le **badge SVG dynamique** dans votre README, site web ou projet en utilisant l’URL publique de Render :

![Zeta Status](https://wewennjr.github.io/zeta-status)

Ou si vous voulez utiliser directement le **fichier JSON ou badge SVG dynamique depuis le serveur Render** :

- Badge SVG dynamique :  
  `https://zeta-ps1y.onrender.com/apiv1/server/badge/status`  

- Fichier JSON du statut :  
  `https://zeta-ps1y.onrender.com/status.json`  
  ```json
  {
      "status": "online"
  }
Ainsi, vous n’avez pas besoin de cloner le dépôt ; vous pouvez simplement faire un fetch ou un curl depuis votre application pour obtenir le statut du serveur en temps réel.

## 🔹 Fonctionnement
Le serveur Render met à jour un fichier status.json via Flask :

"running" → app.py a commencé l’initialisation

"online" → toutes les fonctionnalités prêtes

"stopping" → fermeture en cours (via atexit)

"offline" → serveur éteint ou non joignable

La page GitHub Pages lit ce fichier JSON et affiche le badge avec la couleur et l’emoji correspondant.

Si le serveur ne répond pas, la page affiche automatiquement le badge "offline".

## 🔹 Déploiement
Mettre le fichier index.html dans votre dépôt votre_pseudo.github.io/zeta-status.

Activer GitHub Pages pour ce dépôt.

Accéder à la page publique : https://votre_pseudo.github.io/zeta-status.

## 🔹 Personnalisation
La taille du badge : modifiez width et height dans le SVG.

Les couleurs : modifiez les classes CSS ou le colorMap dans le script JS.

La fréquence de mise à jour : changez l’intervalle setInterval(updateStatus, 5000) en millisecondes.
