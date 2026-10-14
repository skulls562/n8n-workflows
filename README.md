# n8n workflows

Production-style **n8n automations** I build for small teams: AI where it helps, deterministic steps everywhere else, no secrets in the repo.

> I build AI-powered websites and automations. Need one for your business? Write to **jero@dazerit.com** · [dazerit.com](https://dazerit.com) · [Upwork](https://www.upwork.com/freelancers/~01a05884c125d47384)

| Workflow | What it does | Stack |
| --- | --- | --- |
| [AI email digest](workflows/ai-email-digest) | Collects new emails all day and sends one 8:00 summary to Telegram, classified by a **local LLM** into Urgent / Reply / Noise. Email never leaves your machine. | n8n, IMAP, Ollama (Qwen 2.5 7B), Telegram |

More workflows (WhatsApp lead intake, forms → Google Sheets → CRM, AI document drafting) are added as they are cleaned of client data.

## How to use
1. Open n8n → **Workflows → Import from File** and pick the `workflow.json`.
2. Create your own credentials (IMAP, Ollama, Telegram) and replace the placeholders such as `PON_AQUI_TU_CHAT_ID`.
3. Run once manually, then activate.

## Principles
- **No credentials or personal data** are committed; every workflow uses placeholders.
- **Read-only by default**: automations that touch inboxes or customer data never send or delete without an explicit step.
- **Small, testable nodes**: code nodes do one thing and are commented.

---
Built by [Jerónimo Montoya](https://github.com/skulls562), co-founder of [DAZERIT](https://dazerit.com) · MIT License
