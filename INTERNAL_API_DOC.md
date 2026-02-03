# 🧠 GV2-EDGE — Internal API Documentation

---
## universe_loader

load_universe() -> pd.DataFrame

Retourne liste tickers small caps.
event_hub

get_events(tickers) -> dict

Retour :

Json
{
  "TICKER": {
     "event_type": "FDA",
     "impact": 0.8,
     "date": "2026-02-01"
  }
}
nlp_event_parser

parse_event(text) -> dict

feature_engine

compute_features(ticker) -> dict

Retour :
gap, volume, momentum, VWAP, patterns...

monster_score

compute_score(features, events, social) -> float

ensemble_engine

confluence_score(raw_score, signals) -> float

signal_engine

generate_signal(score) -> str

portfolio_engine

calculate_position(capital, risk, stop_distance) -> shares
alerts

send_alert(signal_data)

system_guardian

health_check() -> status
