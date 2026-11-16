---
name: signingflow-download
description: Download the finished Signingflow file after everyone has signed. Use when the person asks for the signed file or the completed document.
---

Call download_signed with envelope set to envelopes/{id}. Return the file only when the envelope is completed. If someone still has to sign, say the file is not ready and do not invent a download link.

This connection cannot read a file from the person's computer.
