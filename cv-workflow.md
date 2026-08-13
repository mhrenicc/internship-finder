# CV workflow — master + per-application variants

## The model

`cv/master.tex` is the **superset**. It holds every credible thing Marko has, in full.
It is never sent to anyone.

Each application gets a **variant**, produced by *cutting and reordering* the master —
never by inventing new content. Subtractive editing keeps every version truthful and
consistent, which matters because interviewers read the version you sent them, not
the one you wish you had sent.

```
cv/master.tex              ← superset, single source of truth
   └── master/*.tex        ← section files
cv/variants/
   ├── optiver-2027.tex    ← one file per application
   ├── google-step.tex
   └── ...
```

## Compiling

There is no LaTeX installed on this machine. Two options:

1. **Overleaf (current setup).** Upload the `cv/` folder, set *Menu → Compiler → XeLaTeX*.
   XeLaTeX is required — pdfLaTeX will fail on the bundled fonts.
2. **Local**, if we ever want it: install MiKTeX (~1–2 GB), then
   `xelatex master.tex`.

## The five tailoring levers

Ranked by how much they move the needle, per application:

| # | Lever | Effort | Notes |
|---|-------|--------|-------|
| 1 | **Summary paragraph** | High | Rewrite all three sentences. Sentence 1 names the role and the company's actual domain. This is the only block a human is guaranteed to read. |
| 2 | **Section order** | Low | Quant → Honors above Experience. SWE → Experience above Honors. |
| 3 | **Skills ordering** | Low | Whatever stack the posting names goes first in its line. Cheap, and it beats keyword filters. |
| 4 | **Bullet selection** | Medium | Keep the bullets that match the posting's verbs, cut the rest to make one page. |
| 5 | **Section inclusion** | Low | Extracurricular is cut first when space is tight. |

## Keyword matching

Many applications pass through an ATS that scores keyword overlap with the posting
before a human sees anything. So for each application:

1. Paste the job posting into the chat.
2. I extract its required and preferred keywords.
3. We check which are **already true** of Marko and surface those in the wording.
4. Anything not true does not go in. Keyword-stuffing gets caught at interview and
   is worse than a missing keyword.

## Hard rules

- **One page** for internship applications, without exception at this career stage.
- **Never list a skill or project that cannot survive a follow-up question.**
- **Every bullet needs a number, or a specific noun.** "Improved performance" is noise;
  "cut p99 latency from 800 ms to 120 ms" is signal.
- **No `\vspace` hacks to cram a second page onto one.** Cut content instead.
- Keep a copy of the exact PDF sent for each application in `applications/` so the
  interview prep matches what they actually read.

## Status

- [x] Master skeleton rebuilt from the Feb 2026 Overleaf source + May 2026 PDF
- [ ] **BLOCKED** — Mindsmiths bullets (needs work laptop notes)
- [ ] Expected graduation date confirmed
- [ ] Year-2 coursework list confirmed
- [ ] Competitive programming handles + ratings
- [ ] LinkedIn URL slug
- [ ] First variant produced
