# Loto Quine

A single-file, offline-first display board for hosting a *loto quine* (French bingo-style
game). Built for organizers to project the drawn numbers on a big screen — no internet
connection, no server, no build step.

## Features

- Full 1–90 board, color-coded as numbers are drawn.
- Large "last number drawn" display, sized for readability from across a room.
- Manual entry: click a cell directly, or type the number and press Enter.
- Duplicate/out-of-range guard with inline error feedback.
- Undo the last draw.
- "New round" to archive the current board and start a fresh grid (for successive games in
  one session: quine, double quine, carton plein...).
- Round history with timestamps and the full draw order of each past round.
- State is persisted to `localStorage`, so an accidental refresh or tab close doesn't lose
  the current game.
- Fullscreen toggle, for projecting on a screen or TV.

## Usage

Open `index.html` directly in any modern browser (double-click it, or drag it into a
browser window). That's it — everything (HTML, CSS, JS) lives in that one file, and nothing
is loaded from the network, so it works with no internet access at all.

## Why a single static HTML file

No framework, no dependencies, no build tooling: for a tool that needs to reliably run
offline on a random laptop connected to a projector, a plain static file is the simplest
thing that can't break.
