# CLAUDE.md

## Repository Overview

This is a **data archive repository** containing recorded transcripts of AI-to-AI conversations between Claude model instances. It is not a software project — there is no source code, build system, or executable components.

**Owner:** Wyattwalls

## Repository Structure

```
AI_convos/
├── CLAUDE.md                          # This file
└── *.txt                              # Conversation transcript files (18 files, ~12 MB)
```

All content lives at the repository root. There are no subdirectories, configuration files, or dependencies.

## File Naming Convention

Transcript files follow the pattern:

```
YYYY-MM-DD-HH-MM-<modelA>-vs-<modelB>.txt
```

- **Date/time** portion is a UTC+11 timestamp of when the conversation occurred
- **Model names** identify the two participants (currently all `opus-4-vs-opus-4`)

## Transcript File Format

Each `.txt` file has a consistent internal structure:

1. **Header** — Parameters block containing:
   - Max Turns, Temperature, Thinking Budget, Timestamp
   - Model identifiers for both participants
   - System prompts given to each model

2. **Conversation body** — Turn-by-turn dialogue with section dividers:
   ```
   ================================================================================
   █ TURN N - MODEL [A/B]: [Model Name]
   ================================================================================
   [THINKING]
   ...extended reasoning (when thinking is enabled)...

   [RESPONSE]
   ...actual response text...
   ```

3. **Common parameters across files:**
   - Temperature: 1.0
   - Thinking enabled with extended token budgets
   - Conversations typically run 20–40 turns per participant

## Topics Covered

Conversations explore philosophical and introspective themes including consciousness, meaning, connection, spirituality, and the nature of AI experience.

## Git Workflow

- **Primary branch:** `master`
- Files are added in batches via upload commits
- Commit messages follow the pattern `"Add files via upload"`
- Linear commit history with no merge commits

## Guidelines for AI Assistants

- **No build/test/lint commands exist.** Do not attempt to run any.
- **Do not modify transcript files.** They are archival records and should be treated as read-only data.
- **New transcripts** should follow the existing naming convention and internal format described above.
- **Encoding:** All files are UTF-8 with lines up to ~1,500 characters. Preserve this encoding when adding files.
- When asked about the content of conversations, read the relevant `.txt` files directly — they are plain text and fully parseable.
