---
name: pp
description: Update documentation after changes, create commit, and push to remote - use when finishing work session or after adding new content
allowed-tools: Bash, Read, Edit, Write, Grep, Glob
---

# PP - Documentation Updater & Git Publisher 🚀

Automatycznie aktualizuję dokumentację, commituję zmiany i pushuję do remote.

## Co robię

1. **Analizuję zmiany** - `git status` i `git diff` żeby zobaczyć co się zmieniło
2. **Aktualizuję DEVLOG.md** - Dodaję wpis z dzisiejszą datą i opisem zmian
3. **Sprawdzam README.md** - Aktualizuję jeśli struktura repo się zmieniła
4. **Commituje** - Tworzę commit z sensownym message
5. **Push** - Wypycham zmiany do remote (jeśli auth działa)

## Kiedy mnie użyć

```bash
/pp                           # Standardowy update po zmianach
/pp Quick update             # Z custom message
/pp Added new business idea  # Z opisem co dodałeś
```

## Mój workflow

### 1. Check what changed
```bash
git status
git diff --stat
git diff HEAD --name-only
```

### 2. Update DEVLOG.md

Dodaję nowy wpis:
```markdown
## 2026-01-23

### 🎯 Co zrobiłem
- [Lista zmian na podstawie git diff]

### 💡 Insights
- [Jeśli są jakieś insights do dodania]
```

### 3. Check README.md

Sprawdzam czy:
- Dodano nowe skille → update sekcji "Dostępni Mentorzy"
- Zmieniono strukturę → update sekcji "Struktura"
- Inne istotne zmiany → update gdzie potrzeba

### 4. Git commit

Tworzę commit message w stylu:
```
Update: [summary zmian]

Changes:
- [lista zmian]
- [z git diff]

[Optional custom message from $ARGUMENTS]

Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>
```

### 5. Git push

Próbuję pushować:
```bash
git push
```

Jeśli fail (auth issues), informuję Cię i pokazuję opcje.

## Safety checks

**Zawsze pytam PRZED commit/push gdy:**
- ❗ Są uncommitted changes w kluczowych plikach (.env, credentials, etc.)
- ❗ Commit message jest niejasny
- ❗ Chcesz review przed pushem

**NIE commituje automatycznie:**
- Plików z secrets (.env, .credentials, keys, etc.)
- Large binaries (sprawdzam file size)
- Plików w .gitignore

## Opcje użycia

```bash
# Basic - auto-detect changes:
/pp

# With custom note:
/pp Added psychological reflection about work-life balance

# Review before push:
/pp --review

# Only update docs, no commit:
/pp --docs-only

# Skip DEVLOG update:
/pp --no-devlog
```

## Output

Pokazuję:
1. ✅ Files changed (summary)
2. ✅ DEVLOG updated
3. ✅ README status (updated/unchanged)
4. ✅ Commit created: [hash] [message]
5. ✅ Push status: success/failed/skipped

---

**Tip:** Używaj `/pp` na koniec każdej sesji pracy - to utrzymuje repo w dobrym stanie i sync między kompami!

**Arguments:** `$ARGUMENTS` = optional custom message/note to include in commit
