# honey-supply-chain-evaluation

Systemdaten der Evaluierung zur Masterarbeit „Transparente Blockchain-basierte Preisbildung in Agrar-Lieferketten“ (Philipp Wildzeiss, 2026). Das Repository ist Teil der Fallstudien-Datenbank nach Yin (2014). Beobachtungsprotokolle, Fragebögen und Transaktions-Hashes sind im Anhang der Arbeit dokumentiert.

## Ordnerstruktur

```
Iteration-1/
  Fallstudie/                 Sitzung mit dem Imker (Sepolia)
  Technischer-Messlauf/       automatisierte Läufe aller Szenarien F-1 bis F-7 (Sepolia)
  Technischer-Messlauf-lokal/ dieselben Läufe auf einem lokalen Hardhat-Node (Osaka)
Iteration-2/
  (gleicher Aufbau)
```

## Dateien

| Datei | Inhalt |
|---|---|
| `measurements-*.csv` | eine Zeile je Transaktion der Fallstudie: Zeitpunkt, Charge, Funktion, Rolle, Transaktions-Hash, Gasverbrauch, Gaspreis, Gebühr, Zeiten für Wallet-Bestätigung und Mining, QI und Preis nach dem Schritt |
| `runs-*.csv` (Fallstudie) | eine Zeile je Charge: Gas gesamt und je Rolle, Gebühr, Endzustand, finaler QI und Preis |
| `runs.csv` (Messlauf) | eine Zeile je Lauf: Szenario, Bienenstand, Gasverbrauch, QI und Preis sowie die Abweichung zur Python-Referenzsimulation |
| `steps.csv` | eine Zeile je Transaktion eines Messlaufs |
| `raw.json` | Rohdaten des Messlaufs |

Zeitstempel sind in UTC angegeben (Ordnernamen ebenfalls). Gaspreise und Gebühren in Wei, Preise in Cent je 500-g-Glas.

## Netzwerk und Softwarestand

| | Netzwerk | Hardfork | Software-Tag |
|---|---|---|---|
| Fallstudie und Technischer Messlauf | Sepolia-Testnetz (Chain-ID 11155111) | Glamsterdam (seit 06.10.2026) | `case-study-iteration-1` bzw. `case-study-iteration-2` |
| Technischer Messlauf lokal | Hardhat-Node | Osaka (Mainnet-Regeln) | wie oben |

Die Contract-Adressen je Iteration sind in den Beobachtungsprotokollen im Anhang der Arbeit angegeben.
