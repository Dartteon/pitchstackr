# Pitch Stack Trainer

A browser-based training tool for [Flesh and Blood](https://fabtcg.com/) players who want to improve their pitch stack recall — one of the most important skills in competitive play.

---

## What is a Pitch Stack?

In Flesh and Blood, cards can be **pitched** (played face-up for resources) to pay for other cards. Pitched cards go to the **bottom of the deck** in the order they are pitched. Because the deck is finite and deterministic, a player who tracks the pitch stack knows exactly which cards are coming and in what order — letting them plan turns many cycles ahead.

Mastering pitch stack recall is considered an advanced skill that separates competitive players from casual ones. This tool lets you practice it in isolation, without the pressure of a real game.

---

## How to Use

1. **Paste your deck** from [Fabrary](https://fabrary.net) — open your deck, tap ⋮ (top right corner) → *Copy card list to clipboard* → paste into the text box.
2. **Set your hand size** (3, 4, or 5 cards per turn — default is 4).
3. Hit **Start with This Deck** and begin training.

Each turn proceeds through two phases:

---

## Game Phases

### Discard Phase

You are dealt a hand of cards. Select any cards you want to **discard** (they go to the Graveyard and are out of the cycle). The remaining cards will be pitched to the bottom of the deck.

- Tap a card to mark it for discard. Tap again to deselect.
- You can also send one card to the **Arsenal** (see Zones).
- Hit **Discard X cards** to confirm. If you discard everything, the pitch phase is skipped.
- **Reset Turn** reverts the entire turn to its starting state.
- **Call Pitch Stack** — at any point, challenge yourself by recalling the full pitch stack from memory.

### Pitch Order Phase

The cards remaining in your hand (after discards and arsenal) need to be pitched. Tap them in the order you want them to arrive back in your hand — **first tap = soonest to draw**.

- Hit **Pitch to bottom of deck** to confirm.
- **Reset** clears your selection so you can re-order.

---

## Zones

### Hand
The cards drawn at the start of each turn. Cards here can be discarded, sent to Arsenal, or pitched.

### Arsenal
A single-card zone that persists between turns — like a held card set aside for later. 

- During the **Discard Phase**, each hand card has an **Arsenal** button. It is only enabled when the Arsenal is empty.
- If you arsenalled the card **this turn**, a **← Hand** button lets you return it.
- If the card was already in the Arsenal from a previous turn, a red **Discard** button lets you send it to the Graveyard.
- Toggle Arsenal on/off using the **Arsenal** button in the footer.

### Graveyard
All discarded cards in the order they were discarded. Scrollable, shown every turn.

### Pitch Stack *(Training Mode only)*
A live view of every card pitched so far, in order. **#1 is the soonest to return to hand**, #N is the deepest. Shown below the Graveyard when Training Mode is ON.

---

## Recall Challenge

At any point during the Discard Phase, tap **☛ Call Pitch Stack** to test your memory. You will be asked to enter every card in the pitch stack in order.

- Tap a slot to open the card picker. Filter by pitch colour (red / yellow / blue).
- Submit your guesses to see a side-by-side comparison with the actual stack.
- Your score is shown as a percentage.

---

## Training Mode

Toggle with the **Training** button in the footer.

| Feature | Training OFF | Training ON |
|---|---|---|
| Deck size | Hidden | Visible |
| Turn counter | Hidden | Visible |
| Pitched count | Hidden | Visible |
| Pitch Stack panel | Hidden | Visible |

Training OFF simulates real game conditions — you have no reference and must recall from memory alone.

---

## Settings (Load Screen)

| Setting | Options | Default |
|---|---|---|
| Hand size | 3 / 4 / 5 | 4 |
| Arsenal | ON / OFF | ON |
| Training | ON / OFF | OFF |

---

## Card Images

Card images are loaded from the official Flesh and Blood card database and cached on first load. Images begin preloading as soon as a deck is pasted — before the game starts — so they should appear immediately once play begins.

If a card image fails to load, the card name and pitch colour are shown as a text fallback.

---

## Deck Format

The app accepts the **Fabrary copy format**:

```
Deck cards
3x Boulder Drop (red)
3x Cranial Crush (blue)
2x Clash of Bravado (yellow)
...
```

Arena cards, equipment, and non-pitched cards are automatically ignored. Only `Deck cards` entries with a `(red)`, `(yellow)`, or `(blue)` suffix are imported.

---

## Hosted On

GitHub Pages — no backend, no login, no data collection beyond anonymous Google Analytics page views.
