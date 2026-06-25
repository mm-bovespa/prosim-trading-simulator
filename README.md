# ProSim – Professional Trading Simulator

**ProSim** is a complete, standalone single-file HTML web application for simulating professional trading strategies with realistic capital management rules.

## Key Features

- **Dynamic Position Sizing**: Every new trade receives `current_cash / (20 - current_open_trades)` as its allocation.
- **Strict Chronological Processing**: On the same day, all sales (cash inflows) are processed **before** new buys.
- **Max 20 Concurrent Positions**: Enforces realistic risk management.
- **Instant Cash Recycling**: Proceeds from closed trades are immediately available for new positions.
- **Detailed Analytics**:
  - Real-time equity curve (Chart.js)
  - Sortable & filterable trade table
  - Event log
  - Summary metrics (Cash, Total Equity, Open Positions, Realized P/L + Win Rate)
- Fully German UI with proper number formatting (`1.234,56 €`)
- Export to CSV and JSON
- Professional dark theme (inspired by TradingView / prop firm dashboards)

## Getting Started

1. Open `ProSim.html` in any modern browser (no installation or server required).
2. Load the built-in example data or paste your own JSON array of trades.
3. Adjust the starting capital if desired.
4. Click **"Simulation starten / Aktualisieren"**.

### Expected JSON Format

```json
[
  {
    "entry_date": "2024-03-12",
    "symbol": "AAPL",
    "entry_price": 178.45,
    "exit_date": "2024-03-19",
    "exit_price": 185.20
  },
  {
    "entry_date": "2024-06-03",
    "symbol": "NVDA",
    "entry_price": 118.20
    // Open position (no exit)
  }
]
```

## Technology Stack

- Tailwind CSS 3.4+ (via CDN)
- Chart.js (via CDN)
- Pure Vanilla JavaScript
- Fully responsive

## License

MIT License – feel free to use and modify.

---

Built as a professional single-file trading tool demo.