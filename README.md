# Maciek -- System Głębokiej Transformacji

Osobiste repozytorium łączące coaching, pracę somatyczną i AI w jedno narzędzie rozwoju. Głębia zamiast powierzchni.

## Co tu jest

```
.
├── coach-memory/              # Pamięć systemu coachingowego
│   ├── profil.md              # Kim jestem -- wartości, sytuacja, patterny
│   └── mapa.md                # Mapa tematów, wnioski, historia sesji
│
├── mems/
│   └── prompty-codzienne.md   # Mikro-prompty, launch codes do stanów mentalnych
│
├── .claude/skills/coach/      # System coachingowy (Claude Code skill)
│   ├── SKILL.md               # Koordynator sesji -- logika, zasady, dispatch
│   └── agents/                # 12 sub-agentów (persony coachów)
│       ├── hudson.md           # Joe Hudson -- emocje, VIEW, klarowność
│       ├── colonna.md          # Jerry Colonna -- shadow work, patterny
│       ├── gervais.md          # Michael Gervais -- performance, peak state
│       ├── silsbee.md          # Doug Silsbee -- ciało, ugruntowanie, obecność
│       ├── march.md            # Steve March -- sens, wypalenie, egzystencja
│       ├── vanderpol.md        # Leon VanderPol -- kryzys, duchowy przełom
│       ├── neill.md            # Michael Neill -- overthinking, prostota
│       ├── litvin.md           # Rich Litvin -- excellent → elite
│       ├── mochary.md          # Matt Mochary -- biznes, energia, delegowanie
│       ├── bailey.md           # Dave Bailey -- skalowanie, founder EU
│       ├── schwartz.md         # Richard Schwartz -- IFS, części, trauma
│       └── hughes.md           # Chase Hughes -- autorytet, czytanie ludzi
│
├── coachowie-gleboka-transformacja-2026.md  # Raport: coachowie głębokiej transformacji
├── top-10-coachow-na-swiecie-2026.md       # Raport: ranking top 10 coachów
├── sesja-hipnotyczna-2020.md               # Notatki z sesji hipnotycznej (2020)
├── schwartz-ifs-transcript.txt             # Transkrypt IFS
├── start.sh                                # Quick launch: claude /coach
└── DEVLOG.md                               # Kronika budowania systemu
```

## Jak używać

### Sesja coachingowa

```bash
./start.sh
```

lub w Claude Code:

```
/coach              # sesja otwarta
/coach reset        # 5 min interwencja
/coach głęboko      # długa sesja w głąb
/coach eksploracja  # nie wiem co jest tematem
/coach [temat]      # konkretny temat
```

System czyta pamięć (`profil.md` + `mapa.md`), prowadzi rozmowę, i w razie potrzeby sięga po perspektywę jednego z 12 coachów. Na koniec sesji aktualizuje pamięć o nowe odkrycia.

### Codzienne prompty

Plik `mems/prompty-codzienne.md` -- zbiór mikro-promptów do pracy z uwagą i stanami. Nie do czytania liniowo. To launch codes: "intencja to system prompt", "jedyną walutą jest uwaga", "teraz: cel czy unik".

## Architektura systemu coachingowego

```
Użytkownik (/coach)
    │
    ▼
Koordynator (SKILL.md)
    │
    ├── Czyta pamięć (profil.md + mapa.md)
    ├── Diagnozuje sytuację
    ├── Prowadzi rozmowę
    │
    ├── Dispatch do sub-agentów (1-3 równolegle)
    │   ├── hudson.md   ← emocje, blokady
    │   ├── schwartz.md ← wewnętrzne konflikty
    │   ├── silsbee.md  ← ciało, somatyka
    │   └── ...
    │
    ├── Synteza perspektyw
    │
    └── Aktualizacja pamięci
```

**Zasady sesji:**
- Jedno pytanie na raz
- Głowa → zapytaj o ciało. Emocje → zapytaj o ciało. Ciało → zapytaj co mówi
- Odkrycie > rada
- Prawda ponad komfort

## Stan projektu

- **9 sesji** przeprowadzonych (luty 2026)
- **12 sub-agentów** -- pełne gremium coachów
- **Pamięć** -- profil + mapa tematów z bieżącą aktualizacją
- **Kluczowe przełomy:** korzeń sabotażu finansowego, blok sprzedażowy (fasolka), relacja ze sobą ("nie zostawię cię"), proszenie o pomoc (taśma), wizja sali audio
