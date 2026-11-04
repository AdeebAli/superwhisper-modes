# Superwhisper modes

My local [Superwhisper](https://superwhisper.com) mode setup. This repo is the live modes folder at `~/superwhisper/modes`, so changes made in the app show up here as uncommitted edits.

## Modes

| Mode | File | Voice model | Language model | Reads | What it's for |
| --- | --- | --- | --- | --- | --- |
| Polish | `polish.json` | Parakeet v3 | Sonnet 5.5 | Active app | Turn dictation into clean written text, matching the format of the destination app |
| Command | `command.json` | Parakeet v3 | Sonnet 5.5 | Selection, clipboard, active app | Speak an instruction to rewrite, answer questions about, or generate text from the source material |
| Command Code | `command-code.json` | Parakeet v3 | Sonnet 5.5 | Selection, clipboard | Speak an instruction to transform code, and get back raw code ready to paste |
| Super | `super.json` | Parakeet v3 | Sonnet 5.5 | None | General dictation cleanup |
| Code Task to Agent Prompt | `code-task.json` | sv-1 | Sonnet 5.5 | Selection, clipboard | Turn a spoken coding task into a structured prompt for an AI coding agent |
| Note | `note.json` | Parakeet v3 | Sonnet 5.5 | None | Dictation cleanup for notes, with speaker separation on |
| Mail | `mail.json` | sv-1 | Sonnet 5.5 | None | Dictation cleanup for email, with a semi-formal tone setting |
| Message | `message.json` | sv-1 | sl-1 | None | Dictation cleanup for messages, with a semi-casual tone setting |
| Offline | `offline.json` | Cohere Transcribe (q4) | s1-mini | None | Dictation using only local models, with no custom prompt |
| Meeting | `system-meeting.json` | Not set | sl-1 | System audio | Meeting capture with speaker separation on, and no custom prompt |
| Polish (Local) | `local-polish.json` | Parakeet v3 | s1-mini | Active app | Polish, using only local models |
| Command (Local) | `local-command.json` | Parakeet v3 | s1-mini | Selection, clipboard, active app | Command, using only local models |
| Command Code (Local) | `local-command-code.json` | Parakeet v3 | s1-mini | Selection, clipboard | Command Code, using only local models |
| Code Task to Agent Prompt (Local) | `local-code-task.json` | Parakeet v3 | s1-mini | Selection, clipboard | Code Task to Agent Prompt, using only local models |

Super, Note, Mail and Message share the same cleanup prompt. "Reads" is the context each mode can send to its language model, and it's worth checking before using a cloud model with sensitive material.

## Models

| Model | Type | Runs |
| --- | --- | --- |
| Parakeet v3 (`nvidia_parakeet-v3_494MB`) | Voice | Local |
| Cohere Transcribe (`cohere-transcribe-q4`) | Voice | Local |
| `sv-1` | Voice | Unconfirmed: no local files found |
| Sonnet 5.5 (`claude-sonnet-5-5`) | Language | Cloud |
| `s1-mini` | Language | Local |
| `sl-1` | Language | Unconfirmed: no local files found, and not in the app's cloud model list |
