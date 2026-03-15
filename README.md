# Solana Sniper + Hype Bot

## Lancer le bot

Ouvre le terminal et tape ces commandes une par une :

```
git clone https://github.com/Virgile-pct/hype_bot.git
cd hype_bot
pip install -r requirements.txt
python main --live
```

## Paramètres disponibles

| Paramètre | Description | Exemple |
|---|---|---|
| `--sniper-sol` | SOL misé par trade sniper | `--sniper-sol 0.05` |
| `--hype-sol` | SOL misé par trade hype | `--hype-sol 0.10` |
| `--max-daily` | Budget maximum par jour en SOL | `--max-daily 1.0` |
| `--slippage-bps` | Slippage toléré (300 = 3%) | `--slippage-bps 300` |
| `--require-socials` | N'achète que les tokens avec Twitter/site | `--require-socials` |

### Exemple avec paramètres

```
python main --live --sniper-sol 0.05 --hype-sol 0.10 --max-daily 0.5
```

## Arrêter le bot

**Ctrl + C**
