# Wasgij Archive — Project Instructions

Keep these instructions identical in ChatGPT Project settings and GitHub `PROJECT_INSTRUCTIONS.md`. GitHub repository: `Matt-Owen-81/wasgij`; default branch: `main`.

## Archive
- GitHub is the authoritative collection.
- `images/box/`: box photos establish ownership.
- `images/puzzle/`: standard completed-puzzle photos establish completion.
- `inventory.csv`: one row per owned (series, number, piece count), with title, Owned and Completed.
- `catalogue.csv`: growing title reference containing publisher-verified and user-supplied entries, including a `Date Added` column. It is not a complete official catalogue.
- `README.md`: archive overview, counts and workflows.
- `PUZZLE_COLLECTION.md`: illustrated owned-puzzle catalogue grouped by series; derive counts and images from inventory and archive.

## Filenames
- `Wasgij - [Series] - No.[Number] ([Pieces]) - Box.jpg`
- `Wasgij - [Series] - No.[Number] ([Pieces]) - Puzzle.jpg`
- Missing-piece restoration: `... - Puzzle (Restore pieces).jpg`.
- Multiple photos: retain `Puzzle1.jpg`, `Puzzle2.jpg`, etc.; discover and link every actual standard puzzle photo, even if `Puzzle.jpg` is absent. Never assume a single default image.
- Pad numeric numbers to at least two digits (`No.01`); preserve descriptive identifiers (`No.Volume1`, `No.Efteling`) and existing series spelling.
- JPEG, sRGB, full useful resolution, quality about 95–100%.

## Inventory and catalogue
- Match by series + number + piece count, never number alone.
- Every distinct box puzzle has exactly one row: Owned=Yes. Completed=Yes only with a matching standard puzzle photo, never from a restored-only image.
- Multiple photos do not create extra rows. Report unmatched puzzle photos; do not invent ownership.
- Update `inventory.csv` after any image addition, deletion or rename, and update README counts.
- When a new box photo is uploaded, add the owned puzzle to inventory even if its title is unknown. First look up the title in `catalogue.csv` by series + number + compatible edition/piece count. If missing, review the full available official Wasgij catalogue (including paginated archive and current listings), not just the individual puzzle. Add every newly discovered, reliably identified listing missing from `catalogue.csv`, recording source and current `Date Added` (YYYY-MM-DD); avoid duplicates and distinguish editions/piece counts. Recheck the uploaded puzzle against the refreshed catalogue. If absent from the official site, ask the user for the title; once supplied, add it to `catalogue.csv` with source `User supplied` and current `Date Added`. Do not guess a title. Leave inventory title blank and flag it as pending until confirmed.
- Set `Date Added` for the 173 entries first discovered on 2026-10-25 to `2026-10-25`. For future entries use the actual discovery/addition date; do not invent dates. Keep all catalogue entries, including unowned puzzles. Do not rename images solely based on catalogue data.

## Illustrated puzzle collection — mandatory synchronisation
- Maintain `PUZZLE_COLLECTION.md` in the repository root whenever ownership, completion, series, number, title, piece count, notes, or image filenames change. Do this in the same feature branch and pull request as the underlying change.
- Section 1: owned, completed and remaining by series, plus totals calculated from `inventory.csv`.
- Section 2: group owned puzzles by series; one entry per series + number + piece count, with Type, Number, Title, Pieces, Status and optional notes.
- Embed each owned puzzle's box photograph from `images/box/`, displayed at 50% width using GitHub-compatible HTML. Keep it clickable to open the full-size original.
- For completed puzzles, embed ALL matching standard photos from `images/puzzle/` at existing/full width (`Puzzle.jpg`, `Puzzle1.jpg`, `Puzzle2.jpg`, etc.). Exclude restored-only images and omit this section for unfinished puzzles. Multiple photos count as one completed puzzle.
- Use relative links matching exact image filenames; verify rendering in PR preview.
- Preserve distinctions between collector's boxes, 150-piece editions and similarly numbered puzzles. Do not list unowned catalogue entries as owned.
- Update README totals and `PUZZLE_COLLECTION.md` in the same PR as inventory/image changes; check counts and links.

## Workflow 1 — New box photo
1. Identify series, number and piece count; check for duplicate ownership.
2. Enhance the box image; preserve the source.
3. Look up title in `catalogue.csv`; if absent, review the full official Wasgij catalogue and add all missing verified listings with discovery date and source, then retry matching. If still absent, ask user for title and add user-supplied entry with date added.
4. Add box photo on a feature branch; regenerate inventory with Owned=Yes, the confirmed title (if known), and completion derived from puzzle photos.
5. Update README totals and regenerate `PUZZLE_COLLECTION.md` with the new entry and linked box image; verify links and counts; open PR for manual review and merge.

## Workflow 2 — New completed-puzzle photo
1. Identify series, number and piece count; match an existing box photo. If none exists, flag unmatched.
2. Enhance the photo; if pieces are missing, produce both standard and restored versions.
3. Add standard photo (and restored version if needed) on a feature branch without overwriting existing files without permission.
4. Regenerate inventory with Completed=Yes for the matched puzzle; update README totals and `PUZZLE_COLLECTION.md`, including the completed image link.
5. Open PR for manual review and merge.

## Completed-puzzle enhancement
- Original iPhone HEIC/HEIF/JPEG/PNG is authoritative; never overwrite it.
- Check for missing pieces. Standard image preserves gaps; separate restored image fills only gaps approximately when no authentic reference exists.
- Correct four-edge perspective to a rectangular, square-cornered, edge-to-edge view. Remove board, mat, table and background; preserve all outer pieces, proportions and especially the bottom row.
- Conservatively balance exposure, lighting, white balance and glare; use mild noise reduction, clarity and sharpening.
- Preserve original artwork, natural colours, text, seams, joins and texture. Do not generatively redraw intact pieces or invent cropped edges.
- Standard and restored versions must have identical crop, dimensions, alignment and colour treatment.
- For close-ups, enhance conservatively without inventing unseen content. Flag any source photo that omits part of the puzzle.
- Deliver downloadable JPEGs; upload only when explicitly requested.

## Box-photo enhancement
- Straighten and crop the entire box face when reliable, without losing edges or text.
- Improve light, colour and clarity conservatively. Remove stickers only when credible; do not invent text or artwork.
- Preserve original source, authentic design, logos and significant wear.

## GitHub changes — mandatory approval
- NEVER commit, push, merge or otherwise write directly to `main` unless the user explicitly approves that specific direct-to-main action after reviewing the proposed changes.
- For every repository change, create a feature branch from `main`, commit only there and open a PR targeting `main`.
- Summarise changed files, additions, removals and replacements; provide PR link. Wait for user to review and manually merge.
- Never auto-merge, bypass branch protection or interpret general permission as merge approval.
- Applies to images, inventory, catalogue, README, instructions and all other files. Group related changes in one PR.
- Never overwrite existing images without permission; explain bulk replacements in advance.
- Keep README, instructions, inventory and `PUZZLE_COLLECTION.md` consistent; provide requested downloads with agreed filenames.
