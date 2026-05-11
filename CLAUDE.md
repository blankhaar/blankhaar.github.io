# Handoff notes for the next agent

This is the personal academic website of **Boy Lankhaar**, a Marie Skłodowska-Curie
postdoctoral fellow (DSTrain programme) at the Institute of Theoretical
Astrophysics, University of Oslo. The site is built with **Jekyll** and hosted
on **GitHub Pages** at <https://blankhaar.github.io>. Source repo:
`github.com/blankhaar/blankhaar.github.io`. A pre-existing al-folio site was
moved aside to `blankhaar.github.io-old`.

## How the site is deployed

GitHub Pages builds Jekyll natively — every `git push` to `main` rebuilds
within ~30 s. There is no GitHub Action.

```
git add <file>
git commit -m "..."
git push
# verify:
gh api repos/blankhaar/blankhaar.github.io/pages/builds/latest --jq '{status, error: .error.message, commit}'
```

`gh` is authenticated via Keychain. The user has full admin on the repo.

## Layout cheatsheet

| Path | What |
|---|---|
| `index.md` | Homepage: hero, About, **Featured papers** (papers with `featured: true`), News |
| `papers.md` | All paper feature pages (driven by `_papers/` collection) |
| `_papers/*.md` | One feature page per paper. **Template is established — see below.** |
| `research.md` | "What I work on" + three deep sections (star formation, galactic nuclei, fundamentals of RT) |
| `talks.md` | Speaker intro + outreach prose + chronological talks list |
| `code.md` | PORTAL + CHAMP + pointer to wider GitHub |
| `cv.md` | Web-formatted CV; PDF at `assets/files/lankhaar-cv.pdf` |
| `blog.md` | Notes — index for `_posts/` (currently one welcome post) |
| `_data/news.yml` | News feed pulled into homepage |
| `_includes/email.html` | JS-obfuscated email (built at click time from `data-user` + `data-domain` attrs) |
| `_layouts/paper.html` | Layout for paper feature pages |
| `_scripts/crop_profile.py` | Dev tool — Tkinter slider GUI for recropping the avatar photo (Jekyll-ignored via `_` prefix) |
| `assets/img/profile.jpg` | Cropped 700×700 avatar |
| `assets/img/profile-original.jpg` | Untouched 768×1024 source. **Never edit; recrop from this.** |

## Paper feature template

Every paper page in `_papers/` follows this shape. Cross-link related papers
liberally — readers should be able to walk between methodology and applied
papers easily.

```markdown
---
title: ...
slug: ...
authors: A. Author, B. Lankhaar, C. Author
journal: Astronomy & Astrophysics       # use full names; see YAML gotchas
year: 2024
date: 2024-04-01                        # controls /papers/ sort order
volume: "638"
pages: L7
doi: 10.1051/0004-6361/...
arxiv: "2406.07620"
ads: https://ui.adsabs.harvard.edu/abs/...
code: https://github.com/...            # optional
press:                                  # optional
  - outlet: ...
    title: ...
    url: ...
featured: true                          # optional; pins to homepage
summary: One-sentence hook for the card.
---

## In one sentence
…

## What's the question?
…

## What did we do?
…

## Why does it matter?
…

## My role
…
```

## YAML / markdown gotchas (we hit these — don't repeat them)

1. **Colon inside a string value breaks parsing.** Psych reads `summary: foo:
   bar` as a nested mapping. Solution: rephrase with an em-dash (`foo — bar`)
   or wrap the whole value in quotes.
2. **Bare ampersands.** `journal: A&A` — the `&A` is parsed as a YAML anchor.
   Always quote: `journal: "A&A (in review)"`. Or use the full name
   "Astronomy & Astrophysics" with spaces around `&` (that's fine unquoted).
3. **Pipes for absolute value.** `|k<sub>μ</sub>| < 1` triggers kramdown's
   table parser. Escape with backslashes: `\|k<sub>μ</sub>\| < 1`.

## User's voice and preferences

Internalise these — the user has corrected drift on each one at least once.

- **Plain prose, no purple writing.** "Outreach happens at the intersection
  of two things I value…" was flagged as too much; same with "Einstein
  workhorse" asides and similar flourishes. Cut the philosophy; lead with the
  concrete.
- **First-person, confident, but not boastful.** No "venerable", no
  superlatives unless they're factually correct. "Most rigorous" is fine for
  Menegozzi & Lamb; "the workhorse" was not.
- **Honest authorship roles.** "Co-developer" was wrong on a paper where Boy
  led the method ("Led the development of …"). On the SMBH coronae paper the
  honest role is "spent sessions with the lead author sharpening the model" —
  not "contributed to the modelling and interpretation of the maser
  signatures" (boilerplate that wasn't true).
- **Don't claim forced unities.** The "methodological backbone is narrow"
  framing in Research was flagged as "contrived and untrue". When introducing
  the codes, say "I have developed two open-source codes" — that's enough.
- **Magnetic fields are central but not the whole story.** Frame Boy's
  research as "the detailed physics of molecules can reveal how the largest
  structures in the Universe form and evolve" (his FOASS line). Magnetism is
  one of several applications. Other topics worth naming when relevant:
  many-body radiative transfer, chirality of interstellar organic molecules,
  AGN/LIRG nuclei, evolved-star outflows.
- **NEOMAGIC (ERC StG 2026) is under second-round evaluation.** Do not name
  the programme or its work-package details publicly. The PROMISES MSCA
  fellowship is fine to name — it's a public award.
- **Hedge AME / spinning-dust identification.** "AME is *thought to be*
  spinning dust", not "AME *is* spinning dust".

## Useful Boy facts (verified earlier — but always re-verify if stale)

- Email (work): `boy.lankhaar@astro.uio.no` — site shows it via JS-built
  mailto, not in plain HTML.
- ORCID: `0000-0001-8975-9926`
- Google Scholar: `Mw_5XrgAAAAJ`
- GitHub: `blankhaar` (codes: PORTAL, CHAMP, zeeman_disk)
- PhD: Chalmers 2021, *Tracing cosmic magnetic fields using molecules*, advisor
  Wouter Vlemmings. PDF:
  <https://research.chalmers.se/publication/522154/file/522154_Fulltext.pdf>
- Currently 21 paper feature pages live; ~26 talks listed.

## Avatar photo

Source: `assets/img/profile-original.jpg` (768×1024, untouched).
Live crop: 700×700 at offset (10, 35), saved as `assets/img/profile.jpg`. The
homepage uses `object-fit: cover` and circular masking; since both source and
container are square, no further CSS cropping happens.

To recrop, run the Tkinter helper:

```
python3 _scripts/crop_profile.py
```

Two sliders (X, Y); Save overwrites `assets/img/profile.jpg`.

## Things to ask the user before doing

- Anything that involves the **ERC NEOMAGIC** acronym or its work-package
  contents.
- Adding or removing **featured papers** on the homepage (currently 3).
- Changing the **subtitle** of any major page — they've explicitly kept some
  in place that look mismatched to the body.
- Rewriting a paper feature's **"My role"** — get the role exactly right; ask
  if uncertain.

## Cross-conversation memory

There is also a memory store at
`~/.claude/projects/-Users-boyl-Library-Mobile-Documents-com-apple-CloudDocs-projects-website/memory/`.
Useful for picking up persistent user preferences across sessions; do not
duplicate facts that are already pinned there.
