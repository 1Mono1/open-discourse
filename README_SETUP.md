# Projekt: open-discourse – Setup und Nutzung für wissenschaftliche Analysen

## Ziel
Dieses Dokument beschreibt, wie du das Projekt für deine Masterarbeit professionell einrichtest und nutzt. Der Fokus liegt auf Datenanalysen mit Python und Docker.

---

## 1. Voraussetzungen
- **Docker Desktop** installiert und gestartet
- **Python** (empfohlen: Version 3.8+)
- **Git** für Versionskontrolle

Node.js und Proxy werden für reine Datenanalysen nicht benötigt.

---

## 2. Projektstruktur
- `database/` – Datenbank-Service (PostgreSQL)
- `frontend/` – Web-Oberfläche (Next.js, optional)
- `proxy/` – API/Proxy-Service (Node.js, optional)
- `python/` – Eigene Analysen und Skripte

---

## 3. Projekt mit Docker starten
1. Öffne PowerShell und navigiere ins Projektverzeichnis:
   ```powershell
   cd 'C:\Users\Notebook\Desktop\open_discourse\open-discourse'
   ```
2. Starte alle Services (Datenbank, ggf. Frontend/Proxy) mit:
   ```powershell
   docker compose up --build
   ```
3. Die Datenbank läuft jetzt im Container und ist bereit für Analysen.

---

## 4. Eigene Analysen mit Python
- Lege eigene Skripte im Verzeichnis `python/src/od_lib/` ab.
- Greife mit Python direkt auf die Datenbank zu (z.B. mit `psycopg2` oder `sqlalchemy`).
- Beispiel für Datenbankzugriff:
  ```python
  import psycopg2
  conn = psycopg2.connect(
      dbname='deine_db', user='dein_user', password='dein_pass', host='localhost', port=5432
  )
  # ... weitere Analyse ...
  ```
- Nutze Jupyter Notebooks für explorative Analysen und Visualisierungen.

---

## 5. Professionelle Arbeitsweise
- **Dokumentiere** alle Schritte und Analysen.
- **Nutze Git** für Versionskontrolle deiner Skripte.
- **Strukturiere** deine Analysen und halte dich an Best Practices (z.B. Kommentare, Linter).
- **Reproduzierbarkeit:** Beschreibe, wie man dein Setup startet und Analysen ausführt.

---

## 6. Troubleshooting
- Fehler beim Starten? Prüfe die Docker-Logs und poste die Fehlermeldung für gezielte Hilfe.
- Node.js/Proxy-Fehler sind für reine Python-Analysen irrelevant.

---

## 7. Weiteres Vorgehen
- Starte mit ersten Analysen in Python.
- Bei Fragen zu Datenbankzugriff, Docker oder Python-Skripten: Hilfe anfordern!

---

## Kontakt & Support
Für Rückfragen oder Hilfe bei spezifischen Problemen kannst du dich jederzeit melden.

---

**Stand:** 13.09.2025
