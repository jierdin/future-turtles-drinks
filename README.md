# Future Turtles Cafe — Drinks & Bar Planning

A free bar/cafe run by camp Future Turtles at Burning Man. No money changes
hands. This repo is the planning and ops toolkit — the drink menu, the
alcohol shopping math, and the bartender-facing checklist — rebuilt (not
started from scratch) each year.

## Start here if you're building next year's version

1. Open `drinks-menu.xlsx` and read its **Start Here** tab first — it
   explains the workbook's own layout, which tabs are for menu design vs.
   procurement, and the house conventions (pour sizes, liquor rules, etc.)
   that were true as of last year.
2. Skim `bar-checklist.odt` to see how the daily open/close routine and
   standing-stock reference were organized — it's written to be read at
   the bar, in the dark, by someone who didn't build the menu.
3. `alcohol-availability-list.xlsx` and `alcohol-shopping-list.xlsx` are
   last year's sourcing research — see "Known year-specific bits" below
   before trusting any prices or availability in them.
4. Treat all of the above as a **starting draft**, not a template to fill
   in blindly — quantities, drink list, and conventions should change with
   headcount, budget, and who's actually running the bar.

## What's in this repo

| File | What it's for |
|---|---|
| `drinks-menu.xlsx` | The core planning workbook: recipes, builds, per-serving costing, purchase list, daily schedule, menu board layout. Start with its own **Start Here** tab. |
| `alcohol-availability-list.xlsx` | Raw research: what alcohol SKUs were available at the sourcing warehouse, with researched prices/sizes. |
| `alcohol-shopping-list.xlsx` | Cross-references the availability list against the drink menu's actual needs to produce a buy list, with a **Read Me** tab explaining the method. |
| `bar-checklist.odt` / `bar-checklist.pdf` | The bartender-facing daily open/close checklist and standing-stock reference, plus day-by-day jug/tea notes. The `.odt` is the editable master; the `.pdf` is a print export of it. |
| `signs-jug-and-tea-4x6.pdf` | Print-ready 4x6 table signage for the jug and tea offerings. (No editable source file exists for this — see below.) |

## House conventions worth knowing before you start editing

These lived in the old `deprecated/` folder as filenames like
`*.bak-20260726-183511-pre-kegswap` — that's gone now (see below), so if
you want the *reasoning* behind a past change, `git log` is where it lives
going forward, not a copy of the file.

## Known year-specific bits to double-check, not assume

- `alcohol-shopping-list.xlsx`'s **Read Me** tab was written for a specific
  warehouse/city and still refers to the *old* filenames
  (`BurningManAlcohol.26.xlsx`, `drinks_menu_no_kegs.xlsx`) from before this
  cleanup — update that tab by hand next time you touch pricing.
- Pricing throughout was researched, not quoted live in-store — expect it
  to be stale by the time you shop.
- `drinks-menu.xlsx`'s Start Here tab documents a year where the bar had
  already moved off kegs onto bottles/cans — don't assume that's still the
  constraint if your setup changes.

## Version control

This project used to track history by hand — duplicate files named things
like `Future Turtles - 2026 Drinks Menu.xlsx.bak-20260726-183511-pre-dirtykeg`.
As of 2026-09-24 it's a git repo instead. Before making a big change,
commit your current state (`git add -A && git commit -m "..."`) rather than
duplicating a file — you get the same safety net without the clutter, and
you can actually diff between versions.

The pre-cleanup snapshot of every file this project ever accumulated
(including the old `deprecated/` folder) is preserved in this repo's first
commit, in case anything in it turns out to still be needed.
