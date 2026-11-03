# Superwhisper modes

My local [Superwhisper](https://superwhisper.com) mode setup. This repo is the live modes folder at `~/superwhisper/modes`, so changes made in the app show up here as uncommitted edits.

## Modes

| Mode | File | Voice model | Language model | Reads | What it's for |
| --- | --- | --- | --- | --- | --- |
| Polish | `new-mode-8.json` | Parakeet v3 | Sonnet 5.5 | Active app | Turn dictation into clean written text, matching the format of the destination app |
| Command | `new-mode-3.json` | Parakeet v3 | Sonnet 5.5 | Selection, clipboard, active app | Speak an instruction to rewrite, answer questions about, or generate text from the source material |
| Command Code | `new-mode-7.json` | Parakeet v3 | Sonnet 5.5 | Selection, clipboard | Speak an instruction to transform code, and get back raw code ready to paste |
| Super | `new-mode-1.json` | Parakeet v3 | Sonnet 5.5 | None | General dictation cleanup |
| Code Task to Agent Prompt | `new-mode-6.json` | sv-1 | Sonnet 5.5 | Selection, clipboard | Turn a spoken coding task into a structured prompt for an AI coding agent |
| Note | `new-mode-2.json` | Parakeet v3 | Sonnet 5.5 | None | Dictation cleanup for notes, with speaker separation on |
| Mail | `new-mode-4.json` | sv-1 | Sonnet 5.5 | None | Dictation cleanup for email, with a semi-formal tone setting |
| Message | `new-mode.json` | sv-1 | sl-1 | None | Dictation cleanup for messages, with a semi-casual tone setting |
| Offline | `offline.json` | Cohere Transcribe (q4) | s1-mini | None | Dictation using only local models, with no custom prompt |
| Meeting | `system-meeting.json` | Not set | sl-1 | System audio | Meeting capture, with no custom prompt |

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
