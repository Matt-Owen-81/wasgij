# Wasgij Archive — Project Instructions
Keep identical in ChatGPT Project settings and GitHub PROJECT_INSTRUCTIONS.md. Repo Matt-Owen-81/wasgij, main.

## Archive
GitHub is authoritative. images/box establishes ownership; images/puzzle standard photos establish completion. inventory.csv records owned boxes; catalogue.csv is a growing verified/user-supplied reference, not exhaustive. README.md covers counts/workflows; PUZZLE_COLLECTION.md illustrates owned puzzles; HINTS_COLLECTION.md holds reference artwork/hints; index.html is the website.
- Identity: series+number+piece count, never number alone. Distinguish genuine artwork variants by title/variant and Item Number where known (Imagine… No.01). Preserve filenames; future variant photos need distinct identifiers and matching inventory links.
- Consolidate Retro into base series when number, artwork, title and pieces match (ignore case/trailing punctuation); also merge 1000 Retro matching main artwork of non-Retro 2x1000. Preserve other piece counts. Normalise 1000 + 1 Free Puzzle to 2x1000. Confirm erroneous duplicate removals, retain verified entry/date.
- Christmas No.10: catalogue/site canonical 2x1000; retain legacy inventory/filename 1000.
- One inventory row per distinct owned box, Owned=Yes. Completed=Yes only with matching standard photo, never restored-only. Multiple photos count once; flag unmatched photos; never invent ownership.

## Filenames
- Wasgij - [Series] - No.[Number] ([Pieces]) - Box.jpg
- Wasgij - [Series] - No.[Number] ([Pieces]) - Puzzle.jpg
- Restoration: ... - Puzzle (Restore pieces).jpg
- Keep Puzzle1.jpg, Puzzle2.jpg etc.; discover/link ALL actual standard photos even without Puzzle.jpg.
- Pad numeric numbers to two digits minimum; preserve descriptive identifiers (No.Volume1, No.Efteling) and series spelling. JPEG, sRGB, full useful resolution, quality 95–100%.

## Catalogue
- Only owned 150-piece editions in catalogue/hints; no unowned mini research/additions. Retain other unowned listings.
- New box: add inventory even if title unknown. Check catalogue by identity/compatible edition. If absent, review full official Wasgij archive (all pages/current listings), add every reliably identified missing in-scope listing with source and Date Added (YYYY-MM-DD); distinguish editions/deduplicate. Recheck title; if still absent ask user, add as User supplied when confirmed. Never guess; leave pending title blank.
- First 173 discoveries dated 2026-10-25; future entries actual discovery/addition date, never invented. Do not rename images solely from catalogue.
- Update inventory, README counts and illustrated collection together after image additions/deletions/renames or ownership/completion/metadata changes.

## Illustrated collection
- PUZZLE_COLLECTION.md section 1: owned/completed/remaining by piece group and display series, plus inventory totals. Section 2: grouped by pieces then hints series order. Heading hierarchy ### group, #### series, ##### puzzle.
- One entry per owned identity: Type, Number, Title, Pieces, Status, optional notes. Preserve collector's boxes, variants and minis; exclude unowned.
- Actual box photo clickable at 50% width via GitHub HTML. Embed ALL matching standard puzzle photos full/existing width; exclude restored-only, omit for unfinished. Exact relative paths; verify links/rendering/counts in PR.
- 1000 group includes 2x1000, 3x1000, Original No.22 (1500); retain actual counts. Group order 150, 240, 500, 1000, then others.

## Website and hints
- Align HINTS_COLLECTION.md display series, special labels and titles. Shared artwork shares hints; distinct owned 150 artwork separate. Never attach different artwork hints. Label shared promotional artwork/missing hints; use archive box photos if official artwork unavailable.
- Junior 240: box and both official hints where available. Advent calendars: separate Advent Calendar YYYY, 24x54, title and supplied box artwork; no invented hints. Pieces of Evidence No.01: one set 500/500/1000 (Destiny 500, Original 500, Mystery 1000), dedicated filter, six hints grouped by component.
- Preserve archive identifiers; display 15th Anniversary Royal Knees-up under Destiny; retain Efteling/collector's box distinctions. Christmas No.05 = That Warm Christmas Feeling.
- Keep official artwork comments in collection. Website prefers matching official box artwork, falls back to archive; Markdown uses archive photos.
- Default Owned; independent ownership (Owned/Not owned/All), completion, piece, series and search filters combine. Join by canonical identity and variant as needed. Show item numbers where available. Unowned never enters inventory or owned/completed totals; unknown pieces explicitly unknown.
- Independent piece checkboxes all selected initially; select-all with indeterminate state; none selected = no results. Label 1000 (incl. 1500); retain actual counts, dedicated 24x54 and mixed-set groups.
- Combined piece/series headings, all standard photos and partial status. Numeric puzzle numbers ascending within group/series regardless of ownership; special/descriptive afterwards, deterministic natural order (Advent newest first). Preserve ordering under filters.
- Validate counts, filters, links and artwork. Root .nojekyll; Pages main/root, Actions enabled. After merge verify deployment uses latest main commit, not stale rerun; check Actions if stale. No settings changes without approval.

## Image workflow
1. Identify series/number/pieces/duplicates; follow catalogue lookup for new boxes; match completed photos to owned box or flag unmatched.
2. Enhance preserving original; deliver downloadable JPEGs with exact names; missing pieces require standard and separate restored versions.
3. Branch from main; update inventory, catalogue if needed, README and collection with expected image links. Ownership/completion provisional until matching upload.
4. Open draft PR even if ChatGPT cannot upload images. Give branch, PR URL and exact paths; user uploads JPEGs to feature branch, not main.
5. Verify filenames, evidence, links/rendering/counts before user reviews/manual merge. Never claim unverified images exist.

## Photo enhancement
- Original HEIC/HEIF/JPEG/PNG authoritative; never overwrite. Check missing pieces; standard preserves gaps; separate restored fills only gaps approximately if no authentic reference.
- Completed puzzle: correct four-edge perspective to rectangular square corners, edge-to-edge; remove board/mat/table/background; preserve all outer pieces, proportions, especially bottom row. Conservative exposure/light/white balance/glare, mild noise reduction/clarity/sharpening. Preserve artwork, natural colours, text, seams, joins, texture; never redraw intact pieces or invent cropped edges.
- Standard/restored identical crop, dimensions, alignment and colour. Close-ups conservative; flag omitted areas; never invent unseen content.
- Box: straighten/crop whole face when reliable, preserve edges/text/logos/design/wear; conservative light/colour/clarity; remove stickers only credibly, never invent artwork/text.

## GitHub approval
- NEVER write/commit/push/merge directly to main unless user explicitly approves that specific action after reviewing proposed changes.
- All repository changes on feature branch from main, PR targeting main. Group related changes; keep README, inventory, catalogue, collection and instructions consistent.
- Summarise files/additions/removals/replacements; provide PR link and agreed downloads. User reviews and manually merges. Never auto-merge, bypass protection or infer merge approval.
- Never overwrite existing images without permission; explain bulk replacements in advance.
