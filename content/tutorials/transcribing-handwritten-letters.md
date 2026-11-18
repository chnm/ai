---
title: "Transcribing Handwritten Letters with a Vision Model (and Checking Its Work)"
dek: "A workflow for using multimodal models on nineteenth-century correspondence, with a verification pass built in from the start."
date: 2026-09-10
image: "https://picsum.photos/seed/transcribing-handwritten-letters/1200/800"
authors: ["Priya Raman", "Tom Velasquez"]
time: "90 minutes"
level: "Intermediate"
tools: ["Any multimodal model", "Spreadsheet", "Image viewer"]
---

Vision-capable language models can now produce a usable first-pass transcription of many nineteenth-century hands. *Usable* is the important word. This tutorial walks through a workflow that treats the model as a fast, unreliable research assistant whose work must always be checked.{{< sidenote >}}Dummy tutorial content for the prototype.{{< /sidenote >}}

## 1. Prepare your images

Crop each page to the text block and save it at a resolution where you can comfortably read it yourself. If *you* can't read it on screen, the model will guess, and its guesses will look confident.

## 2. Ask for a diplomatic transcription

Ask for exactly what is on the page, including errors, strikethroughs, and line breaks. Models tend to "fix" spelling unless told not to.

{{< prompt title="Diplomatic transcription" >}}
Transcribe this handwritten page exactly as written.
- Preserve original spelling, punctuation, and capitalization.
- Mark line breaks with " | ".
- Mark struck-through text as [del: text].
- Mark words you cannot read as [illegible] and uncertain readings as [?word].
Do not summarize, modernize, or correct anything.
{{< /prompt >}}

## 3. Verify line by line

Open the image and the transcription side by side. Check every proper noun, number, and date against the page. These are the places where models fail most often, and they are also the places that matter most to historians.

## 4. Record what you did

Note the model and date in your metadata. A transcription is a derived source, and its provenance belongs in the record.
