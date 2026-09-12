# Plan pracy — lore

## Status audytu
AUDYT ZAKOŃCZONY — 2026-09-12.

## Stan faktyczny
Nowoczesny system kontroli wersji Epic Games, napisany w Rust, zoptymalizowany pod duże binaria i zespoły. README wskazuje stan pre-1.0, centralny content-addressed store, Merkle trees, immutable revision chain, chunking, sparse hydration i SDK dla kilku języków.

## Ryzyka
- API i formaty mogą zmieniać się przed 1.0;
- repozytorium jest upstreamowym projektem Epic Games, więc rebranding wymaga zachowania provenance;
- integracja z UEFN ma opisane ograniczenie względem formatu kompresji;
- krytyczne są testy integralności, kompatybilności i recovery.

## Priorytet
ŚREDNI — wysoka wartość referencyjna.

## Kolejność prac
1. Zmapować crate'y, CLI, serwer i SDK.
2. Zweryfikować testy integralności i recovery.
3. Zbudować macierz platform/toolchain.
4. Ocenić przydatność dla projektów game/asset.
5. Dokumentować lokalne modyfikacje bez zacierania upstream provenance.

## Kryterium zakończenia
Znany jest dokładny zakres lokalnego forka, jego kompatybilność i różnice względem upstreamu; testy integralności i build są reprodukowalne.
