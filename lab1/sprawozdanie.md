# Laboratorium 1 — Podstawy pracy z agentem

Repozytorium GitHub: **DO UZUPEŁNIENIA po utworzeniu repozytorium**

## Informacje diagnostyczne

- Aplikacja: VS Code z Copilot SDK
- Model: `auto` (model wybrany automatycznie przez aplikację)
- Poziom rozumowania: nie był ręcznie ustawiany

## Cel i wykonanie

Uruchomiono przygotowany program `describe_data.py` na pliku
`data/exercise.csv`, zapisując raport do `results/exercise-summary.json`.
Program odczytuje rekordy CSV, zlicza etykiety `ham` i `spam`, a następnie
zapisuje raport JSON z informacją o wejściu, środowisku uruchomieniowym
i sumach etykiet. Nie trenowano modelu.

## Wynik

- liczba wiadomości: **8**
- `ham`: **5**
- `spam`: **3**
- interpreter: Python 3.12.3

Dołączony plik `exercise-summary.json` jest raportem z uruchomienia.

## Weryfikacja

Uruchomiono:

```text
python3 -m unittest discover -s tests -v
```

Wynik: **1 test, OK**. Test używa trzech syntetycznych wiadomości
i sprawdza poprawne zapisanie raportu oraz liczby 3 / 2 / 1. Nie zastępuje
to weryfikacji raportu z `data/exercise.csv`, który został sprawdzony osobno.

## Zapis sesji

Pełny zapis pracy znajduje się w `sesje/sesja-1.jsonl`.
