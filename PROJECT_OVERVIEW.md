# GV2-EDGE — Project Overview

## 🎯 Vision

GV2-EDGE est un système de détection avancé conçu pour identifier le plus tôt possible les **top gainers du marché américain (hors OTC)**, en particulier les small caps à fort potentiel explosif.

L’objectif principal est :

👉 Repérer les actions avant leur forte hausse  
👉 Entrer majoritairement en pré-market ou très tôt en session  
👉 Maximiser les gros movers (+20%, +50%, +100% et plus)  
👉 Gérer le risque de manière professionnelle  

GV2-EDGE ne cherche pas à faire du trading lent ou de petits gains réguliers.  
Il est optimisé pour **capturer les mouvements violents et rapides**.

---

## ⚡ Philosophie du système

GV2-EDGE repose sur 4 principes clés :

### 1️⃣ Détection précoce avant explosion

Le système privilégie :

- Catalysts (FDA, earnings, M&A, upgrades, sector news)
- News multi-sources
- Momentum pré-market
- Patterns historiques de gros winners

Objectif : être **en avance**, pas réactif.

---

### 2️⃣ Confluence intelligente (sans étouffer)

Plutôt que filtrer trop fort :

- chaque signal apporte un boost au score
- les confirmations augmentent la priorité et le sizing

On évite :

❌ trop de règles rigides  
❌ suppression agressive de trades  

On privilégie :

✅ scoring progressif  
✅ hiérarchisation des opportunités  

---

### 3️⃣ Risk management pro mais flexible

- sizing adaptatif (BUY vs BUY_STRONG)
- stops structurels + ATR
- trailing intelligent pour laisser courir les winners
- drawdown control

Objectif : survivre aux séries de pertes et profiter pleinement des gros gains.

---

### 4️⃣ Amélioration continue sans sur-optimisation

GV2-EDGE intègre :

- audits hebdomadaires des top gainers
- attribution de performance par module
- auto-tuning léger du scoring
- backtests manuels réalistes

Mais :

⚠️ sans sur-ajuster  
⚠️ sans casser la robustesse  

---

## 🧩 Briques principales

GV2-EDGE est composé de modules spécialisés :

### 📈 Universe Engine
- Génère l’univers dynamique des small caps US
- Sources Finnhub + IBKR

### 📰 Event Engine
- Collecte multi-source d’événements importants
- Analyse NLP via Grok
- Boost selon proximité et impact

### 📊 Feature Engine
- Momentum
- Volume
- VWAP
- Squeeze metrics
- Patterns winners

### 🌅 Pre-Market Scanner
- Analyse spécifique pré-market
- PM high/low
- breakouts PM
- momentum PM

### 🔥 Monster Score
- Score global pondéré
- intègre events + features + confluence

### 🚦 Signal Engine
- Génère BUY / BUY_STRONG / HOLD

### 💼 Portfolio Engine
- Position sizing automatique
- stops & trailing
- risk control

### 📊 Dashboard
- Temps réel
- opportunités chaudes
- performances
- audits

### 🛡️ System Guardian
- surveillance API
- latence
- santé serveur
- alertes techniques

---

## 📊 Validation & amélioration

GV2-EDGE utilise :

- backtests réalistes timeline
- audits hebdomadaires top gainers
- stress tests
- attribution de performance

Objectif :

👉 savoir ce qui marche vraiment  
👉 renforcer ce qui performe  
👉 garder le système simple et robuste  

---

## 🏆 Ce que GV2-EDGE cherche à optimiser

| Objectif | Priorité |
|---------|---------|
| Détection précoce | ⭐⭐⭐⭐⭐ |
| Capture gros movers | ⭐⭐⭐⭐⭐ |
| Robustesse | ⭐⭐⭐⭐ |
| Simplicité | ⭐⭐⭐⭐ |
| Sur-optimisation | ❌ |

---

## ⚠️ Ce que GV2-EDGE évite volontairement

- trading haute fréquence
- micro-scalping
- règles trop strictes
- indicateurs inutiles
- overfitting

---

## 🚀 Vision long terme

GV2-EDGE est conçu pour évoluer vers :

- meilleure NLP events
- meilleures datas squeeze
- anticipation encore plus fine
- modèles statistiques avancés

Mais toujours avec la même philosophie :

👉 simplicité  
👉 robustesse  
👉 focus sur gros winners  

---

## ✅ En résumé

GV2-EDGE est un système :

✔ orienté top gainers  
✔ axé sur détection précoce  
✔ conçu pour gros rendements  
✔ protégé contre le risque  
✔ évolutif sans complexité inutile  

---

> "EDGE ne cherche pas à gagner tous les jours.  
> Il cherche à être présent sur les jours qui comptent vraiment."

---
