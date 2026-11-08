# Ethan Wu — General Portfolio: Editing Guide

This folder is a clean, plain-HTML version of your general portfolio,
rebuilt from your current site at https://earth325.github.io/portfolio/
(repo `earth325/portfolio`). It is **not** the NCAS version — that lives
separately in `~/workspace/ncas-portfolio/`. This one keeps all your
maker projects and is meant to stay your everyday portfolio.

## Files

- `index.html` — the whole portfolio page (all text and sections)
- `styles.css` — how the page looks (colors, fonts, spacing, photo grid)
- `images/` — all 23 photos from your current portfolio, as separate files
  (no more buried base64 blobs). 22 are used on the page; one spare,
  `first-robotics-5-closeup.jpg`, is in the folder ready to use — swap it
  in by changing a `src="images/..."` value.

## How to change text

1. Open `index.html` in any text editor (VS Code, TextEdit, Notepad, or
   GitHub's web editor).
2. Find the words you want to change and edit only the words between the
   tags. Example: to change a paragraph, edit the words inside
   `<p> ... </p>` — leave the `<p>` and `</p>` tags alone.
3. Helpful comments in the file start with `<!-- EDIT: ... -->` and
   `<!-- MOVE: ... -->` — read those first.

## How to move pictures or sections

- **Move a picture:** cut the whole `<figure> ... </figure>` block
  (from `<figure>` to `</figure>`) and paste it where you want it.
- **Reorder projects:** move a whole
  `<section class="project"> ... </section>` block.
- **Reorder the More Projects entries:** move a whole
  `<article> ... </article>` block.

## How to swap a picture

Easiest: replace the file in `images/` with your new picture, using the
**same filename** (e.g. replace `images/coaster-1-navy.jpg`). The page
updates automatically.

Or: put the new file in `images/` and change the `src="images/..."` value
in `index.html` to the new filename. Always update the `alt="..."` text
too, so it describes the new picture.

## How to add a project

Copy a whole `<section class="project"> ... </section>` block in the
Projects section, paste it where you want it, and change the heading,
text, tags, links, and `src` filenames.

## LinkedIn updates

The Updates section at the bottom of the page
(`<section id="linkedin-updates">`, heading "From LinkedIn") now has
4 entries, added from Ethan's LinkedIn posts:

1. **Hestus — AI for Mechanical Engineering** — company description
   only (Sketch Helper in Autodesk Fusion, 5,000+ engineers, $7.4M seed
   Oct 2, 2026 led by Insight Partners, $8.9M total). Link:
   https://www.hestus.co — Ethan's role is NOT stated; the page
   carries an `<!-- ETHAN: confirm your Hestus connection ... -->`
   comment. Confirm the role (intern, user, collaborator?) and update
   that section before publishing.
2. **StudBud — Cal Hacks 13.0** (Oct 26, 2026) — 36-hour hackathon at
   San Francisco Palace of Fine Arts, AI study companion with Raspberry
   Pi + OpenCV and Anthropic Claude API. Post:
   https://lnkd.in/p/g3E6-9fF — Code:
   https://github.com/ConfidentLetter/CalHacks13.0
3. **CANBus — Tapping My 2015 Prius** (Oct 20, 2026) — ESP32 + ESP-IDF
   TWAI driver parsing raw powertrain hex data, web dashboard, CAN
   High/Low swap, 12V battery ECU reset, rebuild one function at a
   time. Post: https://lnkd.in/p/gxZv3Nve
4. **CAD Challenge at UC Berkeley** (Sep 17, 2026) — biomedical
   engineering theme, collaborated with complete strangers. No
   trophy/placement claimed. Post: https://lnkd.in/p/g4QgbMQS

To add a new LinkedIn post, copy a whole `<article> ... </article>`
block in that section and change the heading, date, text, and link.

## How to publish to GitHub Pages (current portfolio)

1. Go to your repo: https://github.com/earth325/portfolio
2. Replace `index.html` with the `index.html` from this folder.
3. Add `styles.css` and the `images/` folder to the repo (same level as
   `index.html`, not inside another folder).
4. Commit. GitHub Pages rebuilds automatically — wait a minute or two,
   then check https://earth325.github.io/portfolio/

Tip: if you use `git` on your computer instead, copy these three things
into your local clone of the repo, then `git add .`, `git commit`, and
`git push`.

Note: the NCAS portfolio is a **separate** site in a new repo — do not
publish these files there, and do not publish the NCAS files here.

## What's in the portfolio

1. About (first person, updated: DVC Mechanical Engineering student,
   AS completion Aug 2028)
2. Projects — Launch-Pad, bartcv, Coaster, Quad Motor Tester
3. FIRST Robotics — FRC 2204, Fabrication Lead then Team Captain
4. More Projects — Yeti adapter, ThinkPad Hackintosh, solar cooker
5. From LinkedIn — Hestus, StudBud (Cal Hacks 13.0), CANBus Prius project, CAD Challenge at UC Berkeley
