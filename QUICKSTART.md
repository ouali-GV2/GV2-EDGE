# 🚀 GV2-EDGE V2 - Installation Rapide

## 📦 Extraction

```bash
tar -xzf GV2-EDGE-V2-ENHANCED.tar.gz
cd GV2-EDGE-V2-ENHANCED
```

## 🔧 Installation Dépendances

```bash
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

## ⚙️ Configuration

Éditer `config.py` :

```python
# API Keys (REQUIS)
GROK_API_KEY = "votre_clé_grok"
FINNHUB_API_KEY = "votre_clé_finnhub"
TELEGRAM_BOT_TOKEN = "votre_token"
TELEGRAM_CHAT_ID = "votre_chat_id"

# Capital
MANUAL_CAPITAL = 1000  # Votre capital de départ
```

## 🎯 Test Rapide

### 1. Tester Event Hub
```bash
python -c "from src.event_engine.event_hub import get_events; print(len(get_events(['AAPL', 'TSLA'])))"
```

### 2. Tester Signal Logger
```bash
python src/signal_logger.py
```

### 3. Tester After-Hours Scanner
```bash
python src/afterhours_scanner.py
```

### 4. Tester Weekly Audit
```bash
python weekly_deep_audit.py
```

## 🏃 Démarrage

### Mode Production
```bash
python main.py
```

### Mode Debug
```bash
DEBUG_MODE=True python main.py
```

## 📊 Vérification

### Logs
```bash
tail -f data/logs/edge_*.log
```

### Base de données signaux
```bash
sqlite3 data/signals_history.db "SELECT COUNT(*) FROM signals;"
```

### Universe
```bash
cat data/universe.csv | wc -l
```

## 🎓 Documentation Complète

- **Améliorations V2 :** `AMELIORATIONS_V2.md`
- **Changelog :** `CHANGELOG.md`
- **Guide technique :** `README.md`
- **Notes audit :** `AUDIT_NOTES.md`

## ⚠️ Troubleshooting

### Problème : API rate limit
**Solution :** Augmenter `time.sleep()` dans universe_loader.py

### Problème : Database locked
**Solution :** Vérifier qu'une seule instance tourne

### Problème : No signals generated
**Solution :** 
1. Vérifier API keys
2. Check logs dans `data/logs/`
3. Test manuel : `python src/signal_engine.py`

## 🚨 IMPORTANT

Avant production :
- [ ] Configurer API keys
- [ ] Tester 48h en paper trading
- [ ] Monitorer hit rate via audit
- [ ] Valider capital & risque

## 📈 Performance Attendue

- **Hit Rate :** 50-65%
- **Lead Time :** 3-6 heures
- **Early Catch :** 40-50%

Bon trading ! 🎯

---

**Version :** V2.0-ENHANCED
**Support :** Voir AMELIORATIONS_V2.md
