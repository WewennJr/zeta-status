# Zeta Server Status

🚀 Ce dépôt est un GitHub Pages qui affiche le **statut en temps réel** du serveur Zeta.

---

## 🔹 Statuts supportés

| Statut       | Description |
|-------------|------------|
| ⚫ Offline   | Le serveur Render est éteint ou injoignable |
| 🟠 Starting | Render démarre le conteneur et installe les dépendances | (indisponible pour le moment) |
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
