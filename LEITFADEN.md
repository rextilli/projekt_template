Dieser Leitfaden beschreibt die empfohlene Struktur, Arbeitsweise und Best Practices für die Nutzung von GitHub im Team.



Eine gute Projektstruktur

```text
.
├── README.md              # Projektbeschreibung
├── requirements.txt       # Python-Abhängigkeiten
├── src/                   # Quellcode
├── notebooks/             # Jupyter Notebooks
├── data/
│   ├── roh/               # Unverarbeitete Daten
│   ├── verarbeitet/       # Aufbereitete Daten
│   └── beschreibung/      # Datenquellen und Erklärungen
├── results/
│   ├── grafiken/
│   └── tabellen/
├── docs/                  # Dokumentation & Leitfäden
├── CONTRIBUTING.md        # Mitwirkungsregeln, falls notwendig
├── LICENSE                # Lizenz
└── .gitignore             # Ausgeschlossene Dateien, falls vorhanden
```


README.md sollte enthalten:
- Projektbeschreibung
- Übersicht der Ordnerstruktur
- Installationsanleitung (`pip install -r requirements.txt`)
- Links zu Notebooks, Daten und Ergebnissen
- Autor:innen und Lizenz



Eine gute Datenstruktur

 `data/roh/`
Originaldaten (nicht verändert)

 `data/verarbeitet/`
Bereinigte, verwendbare Daten

 `data/beschreibung/`
Quellen, Format-Erklärungen, ggf. ein eigenes `README.md`


 Ergebnisse speichern in
`results/`:
- `grafiken/`: Diagramme, Visualisierungen
- `tabellen/`: Tabellen, CSVs, Zusammenfassungen

Jeder Dateiname sollte Rückschlüsse auf den Inhalt geben.



Notebooks

Jupyter Notebooks für Analysen nutzen (chronologisch und thematisch benennen):

```text
01_datenaufbereitung.ipynb
02_erste_analysen.ipynb
03_visualisierung.ipynb
```




Code-Stil & Tools

### Python:
- `black` – automatisches Formatieren
- `isort` – sortiert Imports
- `flake8` – Linting

```bash
black . && isort . && flake8 .
```

### JS/TS:
- `prettier` – Formatierung
- `eslint` – Linting

```bash
npx prettier --write .
npx eslint .
```

---

Tests (optional)


Tests kommen in den `tests/`-Ordner.


README immer aktuell halten

Jede größere Änderung dokumentieren:
- Neue Skripte oder Daten
- Andere Struktur
- Hinweise zur Ausführung

