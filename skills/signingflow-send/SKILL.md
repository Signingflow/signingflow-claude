---
name: signingflow-send
description: Send an existing Signingflow template or send a reminder. Use when the person asks to send a template for signature or to remind people who have not signed.
---

The workspace is already set. Do not ask for an API key. Do not upload a PDF and do not prepare a draft from a file on the computer. A new file has to be sent from an existing template, or from the Signingflow app.

send_from_template needs template as templates/{id} and recipients with a name and an email. send_reminder needs envelope as envelopes/{id}. A reminder goes only to people who still need to sign that one envelope. It does not change the automatic reminder schedule.

Both tools stop until confirm is true. Set confirm only after the person agrees to that exact send. On CONFIRMATION_REQUIRED, repeat the action and the recipients, then wait. On CAPABILITY_DENIED, WRITES_DISABLED, or HTTP 403, stop. Do not look for another way to send. This connection cannot delete an envelope.
