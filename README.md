# DS Flashcards

A single-file flashcard web app for revising **Distributed Systems** theory, with
**217 question/answer cards** — 178 recall-style cards from the lecture slide decks, plus 39 exam-style theory and reasoning cards.

Everything (cards + styling + logic) lives in **`index.html`** — no server, no internet, no dependencies.

## Features
- **Flip cards** — question on the front, answer on the back. Tap the card (or press Space) to flip.
- **Pick a deck or the whole set** — choose *All decks* for random cards across everything, or a single slide deck at a time from the dropdown.
- **Shuffle** (🔀) for a random order; progress bar and counter show where you are.
- **Mark known** (✓) to track what you've learned; **Hide known** filters those out. Progress is saved in the browser (`localStorage`).
- **Swipe** left/right to move between cards (or use Prev/Next, or ← → arrow keys).
- **Reset** (↺, top right) clears your "known" progress.

## Decks
FT1 Fault Tolerance Basics · FT2 Reliable Multicast · FT3 Message Ordering ·
FT4 Consensus · FT5 Atomic Commitment · Synch (Clocks & Snapshots) ·
Synch (Concurrency, Mutex & Election) · Replication & Consistency · Middleware ·
Big Distributed Systems · ZooKeeper · IoT & WSN · Past Exam (Jul 2017) ·
**Exam-Style · Theory & Reasoning** *(39 theory/discussion cards modelled on written exam questions)*

## Get it on your iPhone (Safari)
Pick whichever is easiest:

1. **AirDrop** — AirDrop `index.html` from your Mac to your iPhone, choose **Save to Files**,
   then open it from the Files app (it opens in Safari).
2. **iCloud Drive** — drop `index.html` into iCloud Drive, open the Files app on the phone,
   tap it → it opens in Safari.
3. **Email/Messages to yourself** — attach `index.html`, open the attachment on the phone.

Then in Safari tap **Share → Add to Home Screen** to get a full-screen, app-like icon
that works completely offline.

> It's one self-contained file with no external resources, so it runs fine straight from
> local storage with no network connection.

## Editing the cards
The cards are a JSON array assigned to `const CARDS = [...]` inside `index.html`.
Each card is `{ "deck": "...", "ref": "...", "q": "...", "a": "..." }`, where `a` may
contain simple HTML (`<b>`, `<ul><li>`, `<table>`). Add or edit entries directly there.
