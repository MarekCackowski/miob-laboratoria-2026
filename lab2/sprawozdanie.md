# Laboratorium 2 — Plan eksperymentu ML

Repozytorium GitHub: https://github.com/MarekCackowski/miob-laboratoria-2026

## Informacje diagnostyczne

- Aplikacja: VS Code z Copilot SDK
- Model: `auto` (model wybrany automatycznie przez aplikację)
- Poziom rozumowania: nie był ręcznie ustawiany

## Plan eksperymentu

Wytrenowano ustalony model na `data/train.csv`, następnie wygenerowano
predykcje dla niewidzianego wcześniej `data/validation.csv`. Oceny dokonano
osobnym krokiem przez połączenie predykcji z etykietami referencyjnymi po ID.
Nie zmieniano hiperparametrów ani danych.

Model to `StandardScaler + LogisticRegression` z `C = 0.01`,
sześcioma cechami numerycznymi i progiem `0.5`. Etykieta, ID i pełny tekst
wiadomości nie były używane jako cechy.

## Wynik walidacji

- wiadomości walidacyjne: **60**
- prawdziwie dodatnie (`tp`): **6**
- prawdziwie ujemne (`tn`): **40**
- fałszywie dodatnie (`fp`): **0**
- fałszywie ujemne (`fn`): **14**
- błędy łącznie: **14**

Plik `metrics.json` zawiera zapisane metryki, a `predictions.csv` predykcje.

## Weryfikacja

Checker eksperymentu zwrócił:

```text
PASS: artifacts support evaluation of the fixed model on the supplied held-out messages.
```

Testy jednostkowe: **3 testy, OK**.

## Zapis sesji

Pełny zapis pracy znajduje się w `sesje/sesja-1.jsonl`.
