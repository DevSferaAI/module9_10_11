# AI with Agent Studio — moduły 9, 10 i 11

Przykłady kodu z kursu: **strategie i wzorce agentowe** (moduł 9),
**halucynacje agentów AI** (moduł 10) oraz **live coding** (moduł 11).
To ten sam kod, który widzisz w lekcjach — sklonuj repo, wpisz swój klucz API
i odpalaj.

## Jak odpalić

```bash
npm install
cp .env.example .env      # i wklej swój klucz z platform.openai.com
npm run 9.2               # odpala przykład z lekcji 2 modułu 9
```

Każdy przykład ma swój skrypt w `package.json` (`npm run 9.4`, `npm run 10.3` itd.).
Wspólny setup (klucz, klient, model) siedzi w `lib/client.ts` — tam zmienisz model,
jeśli chcesz.

## Moduł 9 — Strategie i wzorce agentowe

Jaki kształt ma mieć system, zanim zaczniesz go budować.

| Lekcja | Przykład | Skrypt |
|---|---|---|
| 2. Workflow, czy agent? | ten sam problem raz jako workflow, raz jako agent | `npm run 9.2` |
| 3. Pięć wzorców | routing | `npm run 9.3:routing` |
| 3. Pięć wzorców | ewaluator–optymalizator | `npm run 9.3:ewaluator` |
| 4. Anatomia pętli | żywa pętla: myśl → narzędzie → obserwacja → decyzja | `npm run 9.4` |
| 5. Sterowanie guardraile | limit iteracji + bramka zgody na akcję nieodwracalną | `npm run 9.5` |
| 6. Multi-agent | orkiestrator i wykonawcy | `npm run 9.6` |

Lekcje 1 (Kiedy workflow staje się agentem?) i 7 (Drzewo decyzyjne) nie mają
przykładów kodu.

## Moduł 10 — Halucynacje agentów AI

Żeby agentowi można było ufać.

| Lekcja | Przykład | Skrypt |
|---|---|---|
| 2. Kontekst jako budżet | licznik tokenów: iteracja 1 vs 10 | `npm run 10.2` |
| 2. Kontekst jako budżet | kompakcja rozmowy w trakcie | `npm run 10.2:kompakcja` |
| 3. Pamięć | pamięć między sesjami (plik `pamiec.json`) | `npm run 10.3` |
| 4. Zmyślanie i grounding | halucynacja wywołana na żywo | `npm run 10.4` |
| 4. Zmyślanie i grounding | grounding: wymuszone narzędzie + cytaty | `npm run 10.4:grounding` |
| 5. Evale-observability | LLM-jako-sędzia + test regresji | `npm run 10.5` |

Lekcja 1 (Kontekst, pamięć i zaufanie) nie ma przykładu kodu.

## Moduł 11 — Live coding: wpinamy MCP w agenta

Kod z lekcji live codingu leży w [`Moduł 11 - Live coding/`](<Moduł 11 - Live coding/>).
Bierzemy prostego agenta w LangChain (jedno ręcznie napisane narzędzie, robi
landing page) i wpinamy serwer MCP Gammy — agent dostaje pięć gotowych narzędzi,
których nie piszemy, i sam dobiera parametry prezentacji z jednego zdania.
To osobny projekt z własnym `package.json` — instrukcja w jego README.

## Zasada przewodnia

> Najprostsza rzecz, która zadziała. Złożoność dokładasz dopiero wtedy,
> gdy problem cię do niej zmusi.
