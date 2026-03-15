# Solana Sniper + Hype Bot

Bot de trading automatique sur la blockchain Solana (Pump.fun / Raydium).

---

## Prérequis

Avant de commencer, il faut installer **Python 3.10 ou plus récent**.

- Télécharge Python ici : https://www.python.org/downloads/
- Pendant l'installation, **coche bien la case "Add Python to PATH"**

---

## Étape 1 — Télécharger le projet

Ouvre le terminal (Invite de commandes sur Windows, Terminal sur Mac/Linux) et tape :

```
git clone https://github.com/Virgile-pct/hype_bot.git
cd hype_bot
```

Si tu n'as pas Git, télécharge-le ici : https://git-scm.com/downloads

---

## Étape 2 — Installer les dépendances

Dans le terminal, à l'intérieur du dossier `hype_bot`, tape :

```
pip install -r requirements.txt
```

---

## Étape 3 — Configurer le bot

1. Dans le dossier `hype_bot`, copie le fichier `.env.example` et renomme la copie en `.env`
2. Ouvre le fichier `.env` avec le Bloc-notes et remplis les deux lignes :

```
HELIUS_API_KEY=ta_cle_helius_ici
WALLET_PRIVATE_KEY=ta_cle_privee_base58_ici
```

**Obtenir une clé Helius (gratuit) :**
- Va sur https://helius.dev
- Crée un compte gratuit
- Copie ta clé API et colle-la dans `.env` à la place de `ta_cle_helius_ici`

**Clé privée du wallet Solana :**
- Dans Phantom (l'extension wallet) : Paramètres > Gestion des comptes > Exporter la clé privée
- Colle-la dans `.env` à la place de `ta_cle_privee_base58_ici`
- **ATTENTION : ne jamais partager cette clé avec personne**

---

## Étape 4 — Lancer le bot

### Mode simulation (sans argent réel — recommandé pour commencer)

```
python main
```

Le bot tourne en mode "dry run" : il détecte les opportunités et affiche ce qu'il aurait fait, **sans dépenser de vrais SOL**.

### Mode réel (vrais achats avec ton wallet)

```
python main --live
```

Le bot te demandera une confirmation avant de démarrer. Tape `oui` pour valider.

> **RISQUE IMPORTANT** : le trading de cryptomonnaies comporte un risque de perte totale du capital investi. N'utilise jamais plus que ce que tu peux te permettre de perdre.

---

## Arrêter le bot

Appuie sur **Ctrl + C** dans le terminal pour arrêter le bot proprement.

---

## Fichiers générés

Le bot crée automatiquement deux fichiers dans le dossier :

| Fichier | Contenu |
|---|---|
| `sniper_hype.log` | Journal détaillé de toutes les actions |
| `sniper_trades.csv` | Historique des trades (ouvrable avec Excel) |

---

## En cas de problème

- **"python n'est pas reconnu"** : Python n'est pas dans le PATH. Réinstalle Python en cochant "Add Python to PATH"
- **"pip n'est pas reconnu"** : Même solution que ci-dessus
- **"Module not found"** : Relance `pip install -r requirements.txt`
- **Erreur wallet en mode --live** : Vérifie que ta clé privée dans `.env` est bien en base58 (longue chaîne de lettres et chiffres)
