# Hémicycles belges

**Who voted what, seat by seat.**

An interactive visualisation of roll-call votes in three Belgian assemblies:
the Chamber of Representatives, the Parliament of the French Community
(Fédération Wallonie-Bruxelles), and the Parliament of Wallonia.

Each vote is reconstructed from the assembly's own published transcript and
rendered as a hemicycle: one disc per seat, coloured by political group and
shaped by how that member voted. Hovering a segment of the result bar isolates
everyone who voted the same way; clicking freezes it.

The interface and all editorial content are in French, as are the sources.

**→ <https://hemicycle-be.github.io/hemicycles/>**

## What this is, and is not

A personal, citizen-run project. It is **not affiliated with any political
party**, nor with any of the assemblies whose work it reproduces, and it has no
official standing.

Vote counts, names, group affiliations and quotations are taken verbatim from
the official record. Short titles, summaries and per-group argument syntheses
are written for this site and commit its author alone — they are always kept
visually distinct from the figures.

Work in progress: only a handful of sittings have been processed so far. The
absence of a sitting means nothing more than that the work has not been done
yet.

## Current scope

| Assembly | Seats | Sittings | Roll-call votes |
|---|---:|---:|---:|
| Chamber of Representatives | 150 | 2 | 8 |
| Fédération Wallonie-Bruxelles | 94 | 3 | 13 |
| Parliament of Wallonia | 75 | 1 | 20 |

## Sources

| Assembly | Document | Where |
|---|---|---|
| Chamber of Representatives | Compte rendu intégral (CRIV) | [lachambre.be](https://www.lachambre.be/kvvcr/showpage.cfm?section=/cricra&language=fr&cfm=dcricra.cfm?type=plen&cricra=cri&count=all) |
| Fédération Wallonie-Bruxelles | Compte rendu intégral (CRI) | [pfwb.be](https://www.pfwb.be/agenda) |
| Parliament of Wallonia | Compte rendu avancé (CRA) | [parlement-wallonie.be](https://www.parlement-wallonie.be/pwpages?p=pub-form) |

Walloon *comptes rendus avancés* carry a standing reservation, reproduced on the
relevant pages: they may only be quoted if it is stated that this is a
provisional version binding neither the Parliament nor the speakers.

Members of parliament appear here by name, with how they voted. This is public
information about elected representatives acting in their official capacity,
published by the assemblies themselves.

## Automated checks

Every name list is counted back against the total announced in the transcript.
No member may carry two different group affiliations across a sitting. Every
quotation is located verbatim in the source text and attributed to the speaker
the transcript names. Where the record is silent — a missing first name, a
minister's party, the reason for an absence — the gap is flagged on the page
rather than filled by guesswork.

These checks are programmatic. They catch counting discrepancies, not
misreadings.

## ⚠️ This site may contain errors

Transcripts are parsed and data extracted **by an AI**, with no systematic human
review. Errors of reading, attribution or interpretation remain possible, and
the author cannot be held liable for them.

This is experimental work: doubt is permitted, and even welcome. **Only the
official transcript is authoritative.** To settle a question, follow the source
links above, find the sitting by its date, and read the passage yourself.

## Technical

A single self-contained HTML file. Fonts, party emblems and all data are
inlined: no CDN, no build step, no runtime dependency, no tracking, no cookies.

Routing is fragment-based (`#/wallonie/pw003/7`), so deep links work on any
static host without server rewrites. Display mode (light/dark) is remembered in
`localStorage`; everything else is stateless.

To run it locally, serve the directory with any static server:

```sh
python3 -m http.server 8000
```

## Licence

[GNU AGPL-3.0](LICENSE).

This is not merely a preference. The site embeds a subset of **C059** (URW),
distributed under the AGPL-3 with a font exception that covers inclusion in
PostScript and PDF files only — not in HTML. Embedding it in a web page
therefore places the whole work under the AGPL. Since the site *is* its own
source, the practical cost is nil; anyone reusing it must publish under the same
terms.

Party emblems are the trademarks of their respective owners and are reproduced
for identification purposes only. The Walloon flag is from Wikimedia Commons
(CC0).
