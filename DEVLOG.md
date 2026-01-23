# Devlog - Historia Rozwoju Repo

Log zmian i postępów w budowie personal knowledge base + AI mentorship hub.

---

## 2026-01-23

### ✨ Initial Setup
- Utworzono strukturę repo: `ideas/`, `mems/`, `plans/`
- Dodano `.gitignore` dla macOS `.DS_Store`

### 🤖 Claude Skills System
- Zainstalowano Claude Code CLI (v2.1.17)
- Zrozumiano system skills: personal (`~/.claude/skills/`) vs project (`.claude/skills/`)
- Strategia: project skills w repo dla sync między komputerami

### 📚 Documentation
- Dodano `README.md` z wizją repo jako digital garden
- Dodano `DEVLOG.md` do trackowania postępu
- Koncepcja: skills jako różni mentorzy/eksperci

### 🎯 Pierwsza Skill: Architecture Explainer
- Utworzono `.claude/skills/explain-architecture/`
- Skill do wyjaśniania architektury projektów
- Test git workflow: commit lokalnie ✅, push pending (auth setup)

### 🔮 Roadmap Kolejnych Skills
Planowane "AI Personas":
1. **business-mentor** - Strategia biznesowa, growth, modele biznesowe
2. **psychology-coach** - Psycholog, rozwój osobisty, prywatne rozmowy
3. **research-agent** - Deep research w internecie, fact-checking, analiza danych
4. **creative-writer** - Pomoc w pisaniu, storytelling
5. **productivity-coach** - Time management, produktywność, habits

### 💡 Insights

**Czego się nauczyłem:**
- Skills w `.claude/skills/` są commitowane do git → sync między kompami ✅
- Personal skills w `~/.claude/skills/` są lokalne per komputer
- Skills mogą być używane jako różne "persony" AI - specjaliści w różnych dziedzinach
- Agenci mogą być egzekutorami skills (zobacz Task tool z subagent_type)

**Pytania do eksploracji:**
- Czy można łączyć skills w pipeline? (np. research-agent → business-mentor)
- Jak najlepiej strukturować private reflections w `mems/`?
- Czy skills mogą mieć state/context między wywołaniami?

---

## Template dla przyszłych wpisów:

```markdown
## YYYY-MM-DD

### 🎯 Co zrobiłem
- Bullet points

### 💡 Czego się nauczyłem
- Insights

### 🔮 Następne kroki
- TODOs
```
