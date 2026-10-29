# Missed Call AI Agent for Dentists

An n8n workflow concept for dental clinics that follows up on missed calls through WhatsApp, uses a Gemini-powered agent to understand replies, and helps move suitable conversations toward appointment booking.

## Flow

`Missed-call webhook → WhatsApp message → Patient reply → Gemini AI Agent → Calendar support`

## Included

- Missed-call webhook entry
- Instant WhatsApp follow-up
- Gemini AI conversation handling
- Conversation memory
- Google Calendar booking support

## Setup

Import `workflow.json` into n8n and connect your own WhatsApp, Gemini, Google Calendar, and webhook credentials. Configure clinic details, consent rules, calendar settings, and escalation behavior before activation.

This is a demo workflow and contains no credentials or patient data. It is not medical advice or a replacement for clinic staff.
