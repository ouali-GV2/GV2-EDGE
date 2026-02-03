# 📘 GV2-EDGE — Developer Documentation

## 🎯 Objectif

Ce document explique :

• l’architecture technique  
• le rôle précis de chaque module  
• les flux de données  
• comment étendre EDGE proprement  

---

## 🧱 Vue architecture

main.py ├─ universe_loader ├─ event_hub + nlp_event_parser ├─ social_engine ├─ feature_engine ├─ monster_score ├─ ensemble_engine ├─ signal_engine ├─ portfolio_engine ├─ alerts └─ monitoring

---

## 📦 Modules principaux

### universe_loader.py
Construit l’univers small caps dynamique.

Entrées:
- Finnhub / IBKR

Sortie:
- universe.csv

---

### event_hub.py

Centralise tous les events :

• earnings  
• FDA  
• M&A  
• news  

Appelle `nlp_event_parser.py`.

---

### nlp_event_parser.py

Utilise Grok pour :

• extraire tickers  
• classer type event  
• estimer impact  

Retourne JSON propre.

---

### feature_engine.py

Calcule :

- gap  
- volume spikes  
- momentum  
- VWAP deviation  
- PM levels  
- patterns  

---

### monster_score.py

Combine toutes les features → score unique.

---

### ensemble_engine.py

Renforce signaux par confluence.

---

### signal_engine.py

Transforme score → BUY / BUY_STRONG / HOLD.

---

### portfolio_engine.py

Gère :

• risk %  
• position sizing  
• stops  
• trailing  

---

### system_guardian.py

Surveille :

• APIs  
• ressources  
• erreurs  

---

## 🧪 Backtests

Utiliser uniquement :

backtests/backtest_engine_edge.py

⚠️ Toujours manuel pour éviter sur-optimisation.

---

## 📊 Audits

- weekly_deep_audit.py  
- performance_attribution.py  

---

## 🛠️ Bonnes pratiques

✅ mesurer chaque feature  
✅ éviter ajout inutile  
✅ versionner proprement  
✅ documenter évolution  

---

## 🚀 Ajouter une nouvelle brique

1. créer module dédié  
2. brancher dans main.py  
3. logger impact  
4. tester via audit  

---
