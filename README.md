# Missed-Call AI Agent for Dental Clinics

> A human-handoff workflow concept for responding to missed dental enquiries and moving appropriate conversations toward a booking request.

## The business problem

Missed calls can become lost enquiries, especially after hours. This workflow starts with a missed-call event, sends a consent-aware WhatsApp follow-up, uses an AI agent to understand the reply, and can pass booking context to a calendar step.

## Workflow map

```text
Missed-call webhook
  → WhatsApp follow-up
  → patient reply
  → Gemini conversation agent + memory
  → booking support / human handoff
```

## What it is designed to do

- Start from a missed-call webhook event
- Send an initial WhatsApp follow-up
- Understand basic appointment intent from replies
- Preserve conversation context during the interaction
- Support a calendar-booking step
- Route uncertain or sensitive matters to clinic staff

## What it must not do

- Diagnose, triage clinical emergencies, or provide medical advice
- Make claims about treatment suitability, availability, or pricing without clinic-approved data
- Replace trained staff or a clinic's emergency protocol
- Contact patients without an appropriate consent and messaging policy

## Setup requirements

1. Import `workflow.json` into n8n.
2. Connect your WhatsApp provider, Gemini, Google Calendar, and webhook credentials.
3. Add clinic-specific business hours, approved replies, escalation wording, and staff handoff rules.
4. Define consent, opt-out, privacy, and message-retention policies.
5. Test only with sample data before connecting a live patient channel.

## Privacy and safety

Treat call and message data as sensitive. Use the minimum data necessary, restrict n8n access, avoid putting patient details in logs, and obtain professional compliance advice for the clinic's jurisdiction before deployment.

## Repository contents

| File | Purpose |
| --- | --- |
| `workflow.json` | Importable n8n workflow concept |
| `SECURITY.md` | Security and responsible-use notes |
| `LICENSE` | MIT license |

## License

MIT — see [LICENSE](LICENSE).