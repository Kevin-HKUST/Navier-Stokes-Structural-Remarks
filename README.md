# Three structural remarks on a forced finite-time blowup construction for Navier–Stokes

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22695237.svg)](https://doi.org/10.5281/zenodo.22695237)

Kaiyan Ren — Department of Computer Science and Engineering, The Hong Kong University of
Science and Technology — <krenab@connect.ust.hk>

## What this is

A short **note**, not a research paper. It reads OpenAI's claimed forced finite-time blowup
construction for the 3D incompressible Navier–Stokes equations (made public 8 September 2026)
under the standing assumption that the construction **is correct as claimed**, and records three
structural observations:

1. in a fixed background, the source's `O(N^-1)` bound for the five-moment increment is not sharp;
   the cumulative increment over the full modulation interval is `O(N^-2)`;
2. the terminal force `F_0` is rigidly equivalent to the truncated-shell commutator;
3. at `j_0 = 0` a parity mechanism forces `p_2(·,0) = 0`, so the endpoint cone test (B.19) of the
   source degenerates to `p_1 > 2.2` while `p_1 = 2(3-h)/Λ → 0`; increasing the amplitude `C` does
   not help, because `C` multiplies `p_2`. This degeneration cannot be avoided within the class
   (H1)–(H3) stated in the note.

## What this is not

- **Not a refutation of the source.** `j_0 = 0` lies *outside* the source's domain: the source takes
  `0 < j_0 ≤ .05` and uses the bias deliberately, to break the `z ↦ -z` reflection symmetry.
  Observation 3 says the device fails when *extended* to that external limit point.
- **Not a claim about reflection-symmetric forced blowup**, in either direction.
- **Not a new Navier–Stokes solution**, and not a new regularity criterion.
- **Not complete proofs.** Most propositions carry only an "Argument sketch" and say so explicitly;
  steps tagged `[Assumption]` are unproven. Evidence level is marked inline throughout:
  `[Source]` = verbatim in the extracted text, `[Derived]` = rewriting of source formulas,
  `[Assumption]` = additional hypothesis or unproven step.
- **Not peer-reviewed.**

## Files

| File | Description |
| --- | --- |
| `arXiv Note EN.pdf` | the note (14 pages, A4) |
| `submission-note-en.tex` | source; compiles with XeLaTeX + `article` |
| `arXiv Note EN.pdf.ots` | OpenTimestamps proof for the PDF |
| `LICENSE` | CC BY 4.0 (covers this note only) |

## Persistent identifiers

| Identifier | Value |
| --- | --- |
| DOI — this version (v1) | [`10.5281/zenodo.22695237`](https://doi.org/10.5281/zenodo.22695237) |
| DOI — concept (always the latest version) | [`10.5281/zenodo.22695236`](https://doi.org/10.5281/zenodo.22695236) |
| OpenTimestamps proof | `arXiv Note EN.pdf.ots`; the PDF hash was submitted to the public calendars at the v1 release, and the proof is completable later with `ots upgrade` |
| Software Heritage | archival requested at the v1 release; the SWHID will be listed here once the archive is available |

Cite as:

```bibtex
@misc{ren_stokes_remarks,
  author    = {Ren, Kaiyan},
  title     = {Three structural remarks on a forced finite-time blowup construction for {N}avier--{S}tokes},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.22695237},
  note      = {Preprint; not peer-reviewed}
}
```

The DOI was minted by Zenodo from the GitHub release `v1`, so the archived snapshot and the
publication date are the third-party record of this version; `git` commit dates alone are not.

## Reproducing the line numbers

Every `(lines xxx)` anchor in the note refers to line numbers of a plain-text extraction of the
source PDF, named `navier-stokes.txt`:

- 10264 lines, 507 517 bytes
- 165 page markers of the form `=== PAGE n ===`, no ASCII form-feed characters
- SHA-256 `76a236df4f12ab2261f07047ae56a1dcc320b515c55c82653fea48942b10d674`

Source PDF: linked from OpenAI's announcement page
<https://openai.com/index/navier-stokes-solution/>.

That extraction is a **full-text copy of someone else's paper**, so it is not redistributed here.
The fingerprint above identifies it unambiguously; the author will supply it on request. Two notes
on reproducing it yourself:

- the extraction was `pdftotext`-based, but its version is unknown and the per-page marker format is
  **not** the `pdftotext` default (which paginates with form feeds), so a fresh `pdftotext` run will
  not match the hash byte for byte;
- you do not need it for most checks: the note prints the source's own tags next to each anchor
  (equation numbers such as `(B.19)`, `(10.9)`, statement numbers such as `Prop. B.3 of [S]`), so a
  reader holding the source PDF can locate almost every `[Source]` claim directly.

## Verifying these files

```powershell
Get-FileHash .\'arXiv Note EN.pdf' -Algorithm SHA256
Get-FileHash .\submission-note-en.tex -Algorithm SHA256
```

```sh
sha256sum "arXiv Note EN.pdf" submission-note-en.tex
```

| File | SHA-256 |
| --- | --- |
| `submission-note-en.tex` | `80d8acce1b8b0cbbc739054fee0c1153ce80ed6232dd19f85daeddfa07a09f38` |
| `arXiv Note EN.pdf` | `9bfa04971f5920969717e98bd53fb1e75c07f8f2e8cfacb95dd95c1f80d1017f` |

## Use of AI tools

The note was written with the assistance of generative-AI tools: DeepSeek (line-number extraction,
formula rewriting, parity computations, orchestration of the review rounds), Claude (independent
review, packaging of the release draft), ChatGPT (earlier finite-dimensional notes and material
preparation). These tools are not authors. Every assertion is anchored to source line numbers and
should be checked line by line; tool output is not evidence. The author takes full responsibility
for the entire content, including line-number and scope errors.

## Corrections

Known corrections after the first draft are listed here, so that anyone reading an older copy can
see what changed.

- Note 2, the passage introducing `(10.9)`: an earlier draft wrote that `(3.4)` makes the residual
  vanish identically both for `X ≤ X_ext` and for larger `X`. The source (lines 7349–7350) uses the
  flatness bound `(3.4)` on `X ≤ X_ext`, and the residual vanishes identically only for larger `X`.
  Corrected.

## License

The text of this note is released under CC BY 4.0. This does **not** extend to the source paper or
to any extraction of it, which remain under their own terms.
