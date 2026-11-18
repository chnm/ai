---
title: "From Messy OCR to Structured Metadata"
dek: "Extract names, places, and dates from digitized newspapers into a spreadsheet you can actually audit."
date: 2026-07-22
authors: ["Tom Velasquez"]
time: "2 hours"
level: "Beginner"
tools: ["Python", "Any LLM API", "CSV"]
---

Digitized newspapers come with OCR that ranges from excellent to unreadable. Language models are surprisingly good at reading through noisy OCR to pull out structured information. They are also surprisingly good at inventing it.{{< sidenote >}}Dummy content for the prototype.{{< /sidenote >}}

## The core idea

Ask the model to return structured data *and* to quote the exact text it relied on. The quotation is what makes the output checkable.

```python
fields = ["person", "place", "date", "evidence_quote"]
# Reject any row whose evidence_quote does not appear in the source OCR.
```

## Why the quote matters

If the model's evidence doesn't appear verbatim in the source, the row is either a hallucination or a correction you need to review by hand. A single string-match check catches most fabrications.

## Next steps

Once you have a clean table, the real historical work starts: deciding what the patterns mean.
