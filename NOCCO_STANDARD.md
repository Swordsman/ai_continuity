# NOCCO Protocol
## Nuclear-Option Conversation Carryover

**Version**: 1.0  
**Purpose**: Enable conversation resurrection across different humans and AIs

---

## What is NOCCO?

**NOCCO** is a "resurrection directive" - an instruction to create a document that captures a conversation's semantic meaning and progress so thoroughly that:
- A different human, using a different AI
- Could continue the work (conversation, project, research, discussion)
- With zero wasted effort
- Even if the original participants and all context ceased to exist

**Not just for projects**: NOCCO works for conversations, research, discussions, brainstorming - anything where continuity matters.

---

## Core Principle

NOCCOs are **philosophically immutable** - like conversations themselves, they represent what happened and don't typically change after the fact. However:
- They can be synthesized into larger documents
- They can be combined or analyzed
- Corrections travel as companion pieces (not edits to originals)

**Think of it as**: A conversation snapshot that preserves semantic meaning, not just transcript.

---

## What to Include in a NOCCO

**Essential Elements**:
1. **Context**: Why this conversation exists, background information
2. **Decisions Made**: What was decided and why
3. **Work Completed**: What's been done so far
4. **Current State**: Where things stand right now
5. **Next Steps**: What needs to happen next
6. **Everything for Resurrection**: All information needed to continue

**Optional but Useful**:
- File inventory and locations
- Technical specifications
- Code snippets (not entire files)
- Key references and links
- Open questions
- Alternatives considered

**Not Needed**:
- Complete transcripts
- Tangential discussions (unless they led to decisions)
- Temporary debugging details

---

## Structure Flexibility

There's no mandatory structure. Common approaches:

**Simple** (for short conversations):
- Summary paragraph
- Key decisions
- Next steps

**Standard** (for most projects):
- Executive summary
- Work completed
- Current state details
- Next steps and plan
- Technical details
- Reference material

**Complex** (for large projects):
- Add sections as needed
- Can include: errata, milestones, timelines, risk analysis, etc.

**Rule**: Structure should serve the resurrection goal - include what future participants need.

---

## Naming Convention

Format: `NOCCO_##_[NAME]_##.md`

Example: `NOCCO_01_DASHBOARD_01.md`

**Why numbers in prefix AND suffix?**
Ensures parent NOCCOs and their corrections stay adjacent regardless of file sorting method:
- Alphabetical: prefix sorts together
- Reverse alphabetical: suffix sorts together
- Mixed: one end catches it

**Numbering**:
- First number: sequence in chain (01, 02, 03...)
- Second number: usually same as first
- Corrections: keep same first number, increment second
  - `NOCCO_05_PROJECT_05.md` (original)
  - `NOCCO_05_PROJECT_06.md` (correction)

---

## Creating a NOCCO

**When to create**:
- Conversation approaching token limit
- Major milestone reached
- Before extended break from work
- When context is getting complex
- Before switching to different AI

**How to request**:
> "Create a NOCCO for this [project/conversation/discussion]. 
> Include everything needed for someone else to continue with 
> zero wasted effort."

**AI should**:
- Identify what's essential for resurrection
- Organize information clearly
- Be specific (file paths, versions, dates)
- Include enough detail to continue seamlessly
- Keep it focused (not a transcript, a semantic record)

---

## Using a NOCCO to Continue

**Starting a new conversation**:
1. Upload the NOCCO file
2. Say: "Let's continue from this NOCCO"
3. AI reads and confirms understanding
4. Work continues from where it left off

**If NOCCO is long**:
- AI should read executive summary first
- Skim other sections as needed
- Reference specific sections during work

**If information is missing**:
- Ask for clarification
- Don't assume - resurrection should be explicit

---

## Chains and Trees

**Linear chain** (most common):
```
NOCCO_01 → NOCCO_02 → NOCCO_03 → NOCCO_04
```

**With corrections**:
```
NOCCO_01 → NOCCO_02 → NOCCO_03
                ↓
           NOCCO_03_correction (saved as NOCCO_03_PROJECT_04.md)
```

**Branching** (exploring alternatives):
```
NOCCO_01 → NOCCO_02 → NOCCO_03_optionA
                    ↘ NOCCO_03_optionB
```

**Merging back**:
```
NOCCO_03_optionA ↘
                  → NOCCO_04 (synthesizes both)
NOCCO_03_optionB ↗
```

---

## Corrections and Companions

**Philosophy**: Don't edit published NOCCOs. Create correction companions instead.

**Two approaches**:

**1. Inline errata** (next NOCCO mentions correction):
```
NOCCO_04 includes:
"CORRECTION: NOCCO_02 stated X, should be Y"
```

**2. Companion file** (separate correction document):
```
NOCCO_02_PROJECT_02.md (original)
NOCCO_02_PROJECT_03.md (correction companion)
```

**Benefit**: Even if some NOCCOs in a chain are lost, corrections for surviving ones remain intact.

---

## Multi-AI Usage

NOCCOs work across any AI that can read and understand instructions:
- Claude, GPT, Gemini, DeepSeek, Perplexity, etc.
- Different AIs may have different strengths
- NOCCO preserves continuity regardless of which AI you use

**Switching AIs**:
1. Create NOCCO at end of conversation with AI #1
2. Upload NOCCO to new conversation with AI #2
3. Continue seamlessly

---

## Best Practices

**Do**:
✓ Be specific (file paths, versions, dates, decisions)
✓ Focus on semantic meaning, not transcripts
✓ Include everything needed for resurrection
✓ Create NOCCOs at natural breakpoints
✓ Number consistently for chains

**Don't**:
✗ Wait until token limit (create proactively)
✗ Include tangential discussions without conclusions
✗ Be vague ("we decided on the approach" - which approach?)
✗ Assume context will be remembered
✗ Edit published NOCCOs (create corrections instead)

---

## Example Minimal NOCCO

```markdown
# NOCCO_01_WEATHERAPP_01.md

## Context
Building weather dashboard aggregating 3 APIs. Started Dec 4, 2025.

## Decisions
- React + Node.js + PostgreSQL
- OpenWeather, WeatherAPI, Weatherstack APIs
- Recharts for visualization
- Redis caching (15min TTL)

## Work Completed
- API clients written (src/api/)
- Database schema implemented
- Basic UI components (Header, ForecastCard, SearchBar)

## Current State
- 8 files created, all in Git
- APIs tested, rate limiting works
- Ready for chart integration

## Next Steps
1. Integrate Recharts for forecast display
2. Add error handling UI
3. Deploy to Vercel

## Files
src/api/openweather.js, weatherapi.js, weatherstack.js
src/components/Header.jsx, ForecastCard.jsx, SearchBar.jsx
migrations/001_initial_schema.sql
```

---

## Advanced: Synthesis

Multiple NOCCOs can be synthesized into:
- **Overview documents**: High-level project summary
- **Technical specs**: Combined technical decisions
- **Lessons learned**: Insights across conversations
- **Onboarding docs**: For new contributors

This doesn't replace NOCCOs - they remain as historical record.

---

## Token Counts

NOCCOs typically range:
- **Minimal**: 1-3k tokens (simple conversations)
- **Standard**: 5-15k tokens (typical projects)
- **Comprehensive**: 20-40k tokens (complex multi-phase projects)

Aim for "sufficient for resurrection" not "maximum detail possible".

---

## Version History

**v1.0** (December 2025)
- Initial NOCCO protocol definition
- Multi-AI compatible
- Resurrection directive concept

---

**This document**: Standard reference for NOCCO protocol. Upload to any AI to enable NOCCO usage.

**For minimal version**: See NOCCO_MINIMAL.txt (for custom instructions)
**For full specification**: See NOCCO_SPECIFICATION.md (detailed documentation)
