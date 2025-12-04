# NOCCO Protocol
**Nuclear-Option Conversation Carryover**

Version 1.0 | December 2025

---

## What is NOCCO?

**NOCCO** is a "resurrection directive" - create a document capturing conversation's semantic meaning and progress so thoroughly that a different human with different AI could continue with zero wasted effort.

**Core principle:** Preserve semantic meaning, not transcripts. Enable complete resurrection even if original participants cease to exist.

---

## When to Use

- Token limit approaching (70-80%)
- Major milestone completed  
- Before extended break
- Switching AI assistants
- Context becoming complex

---

## Essential Elements

1. **Context:** Why this exists, background
2. **Decisions:** What was decided, why, alternatives considered
3. **Work Completed:** What's been done
4. **Current State:** Files, dependencies, what works/doesn't
5. **Next Steps:** Immediate, short-term, long-term
6. **Technical Details:** Specs, code, configs
7. **References:** Links, docs, resources

**Exclude:** Transcripts, tangents without conclusions, temp debugging

---

## Structure (Flexible)

```
# NOCCO_##_[PROJECT]_##.md

## Executive Summary
[2-3 paragraphs: current state overview]

## Context/Background
[Why this exists, what problem solved]

## Work Completed
[Done since last NOCCO or from start]

## Current State
[Files, dependencies, what works/doesn't]

## Next Steps
[Immediate → short-term → long-term]

## Technical Details
[Specs, decisions, configs]

## References
[Docs, links, quick reference]

## Meta
[Token count, file locations, how to continue]
```

No mandatory structure - use what serves resurrection.

---

## Naming Convention

Format: `NOCCO_##_[NAME]_##.md`

Example: `NOCCO_01_DASHBOARD_01.md`

**Why duplicate numbers?** Parent and corrections stay adjacent in any sorting.

**Corrections:**
- Original: `NOCCO_05_PROJECT_05.md`
- Correction: `NOCCO_05_PROJECT_06.md`

Keep first number (position), increment second (version).

---

## Creating a NOCCO

**Request:** "Create a NOCCO for this [project/conversation]. Include everything for someone else to continue with zero wasted effort."

**AI should:**
- Identify essential resurrection info
- Organize logically, clear sections
- Be specific: paths, versions, dates, decisions
- Verify: Would this alone suffice?
- Focus: semantic record, not transcript

**Length guidance:**
- Minimal: 1-3k tokens
- Standard: 5-15k tokens  
- Comprehensive: 20-40k tokens

Aim: sufficient for resurrection, not maximum detail.

---

## Continuing from NOCCO

**New conversation:**
1. Upload NOCCO
2. Say: "Continue from this NOCCO"
3. AI reads, confirms understanding
4. Work continues seamlessly

**AI should:**
- Read executive summary first
- Check errata/corrections
- Understand next steps
- Reference sections as needed
- Don't memorize - reference during work

---

## Key Principles

**Philosophical Immutability:** NOCCOs represent conversations that happened. Don't typically change. But can be: synthesized into larger docs, combined/analyzed, referenced/built upon, edited for typos (substantive changes = create correction).

**Corrections Travel Adjacent:** Filename ensures corrections stay with originals.

**Multi-AI Compatible:** Works with Claude, GPT, Gemini, DeepSeek, Perplexity, etc. Switch by creating NOCCO → upload to next AI.

**Not Just Projects:** Conversations, research, discussions, creative work - anything needing continuity.

---

## Chains and Trees

**Linear (most common):**
```
NOCCO_01 → NOCCO_02 → NOCCO_03 → NOCCO_04
```

**Branching (alternatives):**
```
NOCCO_01 → NOCCO_02 → NOCCO_03_optionA
                    → NOCCO_03_optionB
```

**Merging (synthesis):**
```
NOCCO_03_optionA ↘
                  → NOCCO_04 (combines)
NOCCO_03_optionB ↗
```

---

## Best Practices

**Do:**
- ✓ Be specific (paths, versions, dates, exact decisions)
- ✓ Focus on semantic meaning, not transcripts
- ✓ Include everything for resurrection
- ✓ Create proactively (don't wait for limit)
- ✓ Test: Could someone else continue from this?

**Don't:**
- ✗ Be vague ("the approach" - which?)
- ✗ Assume context ("obviously Python" - state it)
- ✗ Wait until 95% token limit
- ✗ Include full transcripts
- ✗ Edit for substantive changes (create correction)

---

## Resurrection Test

NOCCO passes if, given only the file, competent person + AI could:
- Understand what was being done
- Understand why decisions made
- See current state clearly
- Continue work seamlessly
- Not redo anything done

---

## Example Minimal NOCCO

```markdown
# NOCCO_01_WEATHERAPP_01.md

## Context
Building weather dashboard aggregating 3 APIs. Started Dec 4, 2025.

## Decisions
- React + Node.js + PostgreSQL
- OpenWeather, WeatherAPI, Weatherstack
- Recharts for viz, Redis caching (15min)

## Work Completed
- API clients (src/api/)
- Database schema
- UI components (Header, ForecastCard, SearchBar)

## Current State
- 8 files, all in Git
- APIs tested, rate limiting works
- Ready for chart integration

## Next Steps
1. Integrate Recharts
2. Add error handling UI
3. Deploy to Vercel

## Files
src/api/openweather.js, weatherapi.js, weatherstack.js
src/components/Header.jsx, ForecastCard.jsx, SearchBar.jsx
migrations/001_initial_schema.sql
```

---

## Quick Start

1. Work with AI on project
2. At natural breakpoint: "Create a NOCCO"
3. AI generates comprehensive snapshot
4. Download and save
5. New conversation: Upload NOCCO, "Continue from this"
6. AI reads and continues seamlessly

---

**NOCCO v1.0 (December 2025)**

This document is optimized for AI assistant fetching. Reference in custom instructions or conversations.
