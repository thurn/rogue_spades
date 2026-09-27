# Rogue Spades Deck Archetypes

A deck archetype answers one question: **how is this player going to win the
game?** Each archetype below is a coherent plan that a player can recognize in
the shop, commit to over several purchases, and execute at the table.

This document is a design target, not a sigil list. Sigils named here are
illustrative; the numbered references (`#1`–`#12`) point to the example sigils
in the game overview.

## Rules Context

These are the rules the archetypes are built against.

- **Scoring:** standard Spades. Made contract = 10 × bid + 1 per overtrick
  (bag). Set = −10 × bid. Every 10 bags = −100. Nil = ±100, blind nil = ±200.
- **Win condition:** first partnership to 500 wins. If nobody reaches 500 after
  13 rounds, the higher score wins.
- **Gold:** after each round you gain gold equal to your partnership's round
  score. Negative rounds grant 0 gold.
- **Shop:** after each round, buy at most one of three offered sigils. Rerolls
  are allowed.
- **Collection:** you own sigils, not cards. Each deal, your whole collection is
  re-engraved onto your new 13-card hand, one sigil per card at most. Affinity
  sigils go to a matching card when possible; the rest land randomly.
- **Ranks:** integers from 2 to 14 (ace), clamped at both ends. When two cards
  of the same suit and rank meet in a trick, **the one played second wins**.
- **Suit conversion:** a converted card is fully that suit — it follows, trumps,
  and breaks spades as that suit. Duplicate cards are allowed.
- **Passing:** only a nil (or blind nil) bidder trades 2 cards with their
  partner. Sigils travel with passed cards.
- **Information:** you see your own sigils. Other players see a sigil only when
  it activates. Each partnership's full collection is visible on a pre-round
  scouting screen, but not which card carries what.
- **Opponents** have sigils too. A multiplayer mode may make the partner human.

### Numbers that shape every archetype

- **The clock.** 500 points in 13 rounds is ~39 points per round — roughly a
  made partnership bid of 4 every hand. Anything that averages above that wins
  on pace; anything below it must win on the round-13 score comparison.
- **Nil is enormous.** A made nil plus a partner making 3 is 130 points — a
  third of the game in one round. A failed nil is −100 and 0 gold.
- **Gold is points.** A strong round both advances the score *and* buys the next
  sigil. A set round stalls both. Consistency compounds.
- **~12 purchases.** One sigil per shop over 13 rounds means a finished deck has
  roughly a dozen sigils. The 13-sigil cap is rarely the constraint; shop luck
  and reroll gold are.
- **The ace cap wastes rank.** `#5` Becomes ace on an ace does nothing, and `#1`
  +10 on a king is +1. High-rank builds hit diminishing returns fast.
- **The tie rule rewards position.** With many cards clamped to ace (or to 2),
  ties become common, and the later player wins them.

### Recurring archetype needs

Random engraving means every archetype has the same three shopping needs:

- **Enablers** make the plan possible (e.g. convert cards to spades).
- **Payoffs** make the plan worth doing (e.g. gain points on ruff).
- **Consistency** makes the plan work on any deal: affinity sigils, global
  effects, or sigils that do not care which card they land on.

An archetype with enablers but no payoffs is just "a slightly better hand." An
archetype with payoffs but no consistency is a slot machine.

---

## The Archetypes

### 1. Ghost — Nil Every Round

**Win plan:** Bid nil every round and let the +100 carry the partnership to 500
in four or five rounds.

- **Scoring:** nil (+100) plus partner's bid. At 130/round, the game ends by
  round 4.
- **Enablers:** rank reduction (`#3`, `#4`), `#8` Affinity face cards → low spot.
- **Payoffs:** anything that rewards a made nil (bonus gold, bonus points), and
  "when this loses a trick" triggers.
- **Consistency:** affinity for face cards is critical — a single unlowered king
  in a short suit sinks the round.
- **Play pattern:** pass your two most dangerous cards to partner; duck
  everything; slough high cards the moment you are void.
- **Tie hazard:** ranks clamp at 2, so a lowered card can *tie* a real 2. If an
  opponent leads the 2♥ and you must follow with a lowered 2♥, **you win the
  trick**. Ghost wants to play *first* on low-card ties, the opposite of most
  builds.
- **Weaknesses:** a single set costs 100 points and a round of shopping.
  Opponent sigils that force you to win, or that raise your ranks, are lethal.
- **Pairs with:** Kingmaker, Conduit, Bag Bomber.

### 2. All In — Blind Nil

**Win plan:** Bid blind nil for ±200 on hands you have not seen, relying on a
collection that makes *any* deal safe.

- **Scoring:** a made blind nil is 200 points. Two of them plus modest partner
  bids is a win.
- **Distinct from Ghost:** Ghost bids after seeing a hand; All In bids before.
  All In therefore cannot rely on affinity luck — it needs effects that work
  regardless of which cards arrive.
- **Enablers:** global "while held" or round-start effects that lower ranks
  across your hand, and bid-time reveals that protect nil bids.
- **Payoffs:** the 200-point swing itself; sigils that improve blind-nil passing
  (extra cards, choosing after seeing partner's hand).
- **Weaknesses:** extremely high variance; one failure is −200 and zero gold.
  Opponents who scout a blind-nil collection will lead to bust it.
- **Pairs with:** Conduit (passing is the only way to fix a bad blind hand).

### 3. Crown — High Ranks, Big Bids

**Win plan:** Push every card toward ace and make partnership bids of 8–10,
scoring close to 100 per round.

- **Scoring:** a made 10-bid is 100 points; five of those wins.
- **Enablers:** `#1`, `#2`, `#5`, `#6`, `#7` Affinity low spots → face card,
  `#12` adjacency bonuses.
- **Payoffs:** "when this wins a trick" triggers; bid-time reveals that multiply
  large bids.
- **Consistency:** `#7` is ideal because it targets the cards that need help.
  Flat +rank sigils landing on face cards are wasted by the ace cap.
- **Play pattern:** bid aggressively, play late in tricks where possible, draw
  trump early so your off-suit aces cash.
- **Weaknesses:** aces lose to any spade once a player is void. Duplicate aces
  lose ties to whoever plays later. A big set (−100) is devastating.
- **Pairs with:** Closer (wins the ace-vs-ace fights), Trump Lord.

### 4. Trump Lord — Spades Everywhere

**Win plan:** Convert as much of the hand to spades as possible and win tricks
by trumping, so off-suit rank barely matters.

- **Scoring:** reliable 5–7 trick bids from sheer trump count.
- **Enablers:** `#9` Non-spade becomes spade, rank boosts on spades.
- **Payoffs:** "on ruff" triggers — points, gold, or rank buffs when you trump.
- **Play pattern:** stay void in a side suit so you can ruff early; once spades
  are broken, lead trump to strip opponents.
- **Rules friction:** you cannot lead spades until broken unless your hand is all
  spades, so a near-all-spade hand wants to go *all* the way. Converted spades
  can duplicate real ones, and the tie rule decides who wins.
- **Weaknesses:** opponents with their own spade conversions contest trump.
  Converting low cards gives many small spades that lose to real high ones.
- **Pairs with:** Void Dancer, Crown.

### 5. Monosuit — Own One Off-Suit

**Win plan:** Concentrate one non-spade suit (hearts, diamonds, or clubs) and
win the long tail of that suit after trump is drawn.

- **Scoring:** moderate bids built on 4–6 length tricks, plus suit-specific
  payoffs.
- **Enablers:** `#10`, `#11` suit conversion; suit affinity sigils.
- **Payoffs:** conditionals like "when played to a diamonds trick," "while you
  hold 5+ diamonds," and effects that stop your suit from being trumped.
- **Play pattern:** let partner or your own spades draw trump, then run the suit.
  `#12` adjacency naturally clusters in a long sorted suit.
- **Weaknesses:** holding most of a suit makes everyone else void in it, so
  without anti-ruff protection your long suit becomes their trump bait.
- **Pairs with:** Slow Burn, Closer. **Conflicts with:** Void Dancer in opponent
  hands (your length creates their sloughs).

### 6. Void Dancer — Profit From Sloughing

**Win plan:** Engineer voids and generate points every time you throw off a card
without following suit.

- **Scoring:** a low, safe bid (2–3) plus a steady stream of slough-triggered
  points.
- **Enablers:** suit conversion that empties side suits (the same sigils Trump
  Lord and Monosuit want).
- **Payoffs:** "when thrown off" / "on slough" triggers: points, gold, or buffs
  to your remaining cards.
- **Play pattern:** get void early, then decline to ruff so the trigger fires.
  Choosing between ruffing and sloughing each trick is the core skill.
- **Weaknesses:** a balanced deal gives few voids. Every slough is a trick you
  did not win, so the contract must stay small.
- **Pairs with:** Trump Lord (conversion creates voids), Merchant, Bag Bomber.

### 7. Closer — Win on Position

**Win plan:** Win tricks by playing last. Exploit the "second played wins ties"
rule and the ace cap to beat equal cards cheaply.

- **Scoring:** mid-sized bids that are unusually safe, because you win the fights
  you pick.
- **Enablers:** `#5` Becomes ace and `#6` Becomes king create duplicate top cards;
  sigils that change who leads.
- **Payoffs:** "when played fourth," "when this wins a tie," and seat-control
  effects.
- **Play pattern:** hold duplicates until an opponent commits their top card,
  then match it from a later seat. Avoid leading.
- **Weaknesses:** needs the lead to fall to others. Opponents who scout ace-making
  sigils will hold their own aces until after you play.
- **Pairs with:** Crown (the ace flood makes ties common), Monosuit.

### 8. Slow Burn — Power From Holding

**Win plan:** Hoard "while held" cards that grow stronger each trick, then cash a
guaranteed endgame.

- **Scoring:** bids built on the last 3–5 tricks being certain wins.
- **Enablers:** "while held" sigils that scale per trick or buff other cards.
- **Payoffs:** the final tricks, plus global "while held" auras (e.g. your suit
  cannot be trumped while this card remains).
- **Play pattern:** stay void in the suit of your held cards so you are never
  forced to play them early.
- **Weaknesses:** following-suit rules can force a held card out prematurely.
  Early tricks are weak, so a set is possible if the endgame is disrupted.
- **Pairs with:** Monosuit, Contractor (the endgame is predictable).

### 9. Conduit — Passing as a Weapon

**Win plan:** Use passing to move sigiled cards to where they do the most good,
turning two hands into one optimized unit.

- **Scoring:** partnership bids made more reliable by trading after bidding.
- **Rules hook:** baseline passing only happens on nil bids, so Conduit either
  bids nil or buys sigils that grant extra or unusual passing.
- **Enablers:** extra pass count, passing without nil, passing to opponents.
- **Payoffs:** "when passed" triggers; "cursed" cards that punish whoever holds
  them — pass them to an opponent.
- **Play pattern:** read your partner's bid, then hand them your trump and aces
  while pulling back their danger cards.
- **Weaknesses:** depends on nil or rare passing sigils; the pass happens after
  bidding, so misjudging partner's needs is permanent.
- **Pairs with:** Ghost, All In, Kingmaker. Especially strong in multiplayer
  with a human partner.

### 10. Kingmaker — Build Your Partner

**Win plan:** Turn your partner into the powerhouse. Your losing cards buff their
hand and their contract.

- **Scoring:** partnership points count the same regardless of who takes the
  trick. You bid low; partner bids high.
- **Enablers:** "when this loses a trick" and "when played" effects that raise
  partner's ranks or protect their bid.
- **Payoffs:** partner-bid multipliers, gold on partner tricks.
- **Play pattern:** sacrifice tricks deliberately. In single-player, this gives
  the sigil-less AI partner real power.
- **Weaknesses:** you do not control partner's play. If partner is set, your
  investment is wasted.
- **Pairs with:** Ghost, Conduit.

### 11. Contractor — Bend the Bid

**Win plan:** Change what bids are worth. Make exact contracts and multiply their
value with bid-time sigils.

- **Scoring:** fewer tricks, bigger numbers per trick bid.
- **Enablers:** bid-time reveals: "your bid counts double if made," "adjust your
  bid by 1 after the first trick," "+50 for making your bid exactly."
- **Payoffs:** the multiplied contract itself.
- **Play pattern:** bid only what is certain; avoid overtricks, which are wasted
  or penalized under exact-bid effects.
- **Weaknesses:** a doubled set is doubled too. Opponents who scout bid sigils
  will target your contract.
- **Pairs with:** Slow Burn, Closer. **Conflicts with:** Sandbagger.

### 12. Sandbagger — Bags Are Income

**Win plan:** Bid low, take extra tricks every round, and use sigils that turn
bags from a liability into points.

- **Scoring:** low bids (almost never set) plus many overtricks. Vanilla bags are
  only +1 each and −100 per ten, so this archetype *needs* payoffs.
- **Enablers:** anything that makes a hand stronger than its bid.
- **Payoffs:** "+X points per bag," "raise the bag penalty threshold," "reset your
  bag count," "bags earn bonus gold."
- **Play pattern:** always underbid; never be set; win every trick you can.
- **Weaknesses:** before the payoffs arrive, the build is actively losing to the
  bag penalty. Slow against the 39-per-round clock.
- **Pairs with:** Crown, Merchant. **Conflicts with:** Contractor.

### 13. Merchant — Points Outside the Contract

**Win plan:** Score through triggers rather than bids. Because gold equals
points, the income snowballs into a stronger collection.

- **Scoring:** small triggered points on wins, losses, plays, and sloughs, adding
  30–60 per round on top of a modest contract.
- **Enablers:** gold-for-rerolls, which is how this archetype finds its pieces
  faster than others.
- **Payoffs:** "when this wins a trick, +10 points," "when played to a heart
  trick, +5 points," and similar flat income.
- **Play pattern:** play to trigger sigils, not just to take tricks. Contract
  safety comes second to trigger count.
- **Weaknesses:** slow early; many small triggers are easy for opponent sigils
  to shut down with global rule changes.
- **Pairs with:** almost anything as a secondary plan; especially Void Dancer and
  Sandbagger.

### 14. Spoiler — Set the Opponents

**Win plan:** Win the round-13 score comparison by keeping opponents from
scoring. Every set costs them 10 × bid, and every busted nil costs them 100.

- **Scoring:** your own modest bids plus large opponent losses. You do not need
  to reach 500 — you need to be ahead after round 13.
- **Enablers:** bid-time reveals that punish high opposing bids; round-start
  reveals that change the rules *after* opponents have already bid.
- **Payoffs:** "when this wins a trick an opponent needed," nil-busting triggers.
- **Play pattern:** read the scouting screen, then aim sigils at the opponents'
  plan. Force the opposing nil bidder to win a trick.
- **Weaknesses:** depends on opponents bidding aggressively; a cautious opposing
  AI gives few targets. Slow; relies on the timeout rule.
- **Pairs with:** Lawgiver, Bag Bomber.

### 15. Bag Bomber — Force Overtricks on Opponents

**Win plan:** Make opponents take tricks they did not bid for until the bag
penalty breaks them.

- **Scoring:** −100 to opponents every 10 bags, plus your own contract.
- **Distinct from Spoiler:** Spoiler wins tricks to set opponents; Bag Bomber
  *loses* tricks to overload them.
- **Enablers:** "when this loses a trick, the winner gains an extra bag"; effects
  that make opponent tricks count double for bags.
- **Payoffs:** the bag penalty itself, plus triggers on reaching a bag threshold.
- **Play pattern:** duck tricks your opponents must take; bid low so ducking does
  not endanger your own contract.
- **Weaknesses:** slow burn on the score; opponents who bid high absorb the
  tricks as made contract instead of bags.
- **Pairs with:** Ghost (every ducked trick is a bomb), Void Dancer, Spoiler.

### 16. Lawgiver — Rewrite the Round

**Win plan:** Build a collection around global rule changes, so each round is
played under rules your hand was designed for.

- **Scoring:** whatever the rule enables — often a large made bid on a rule-bent
  round.
- **Enablers:** bid-start reveals ("hearts are trump this round," "no trump")
  and round-start reveals ("lowest card wins," "all 7s are aces").
- **Timing matters:**
  - **Bid-start** reveals change the rules before bidding. Everyone adapts, but
    only you built your collection for it.
  - **Round-start** reveals change the rules after bidding. Opponents' bids are
    now wrong — a Spoiler tool.
- **Payoffs:** sigils that only work under your chosen rule (e.g. low cards
  engraved to trigger when "lowest wins" is active).
- **Weaknesses:** rule sigils land on random cards and may conflict with each
  other. Opponent rule sigils can override yours.
- **Pairs with:** Spoiler, Ghost (a "lowest wins" round turns a nil hand into a
  powerhouse — and vice versa).

---

## Summary Table

| # | Archetype | Win path | Pace | Variance |
|---|-----------|----------|------|----------|
| 1 | Ghost | Nil every round | Very fast | High |
| 2 | All In | Blind nil | Very fast | Extreme |
| 3 | Crown | Big made bids | Fast | Medium |
| 4 | Trump Lord | Trump everything | Medium | Low |
| 5 | Monosuit | Long off-suit | Medium | Medium |
| 6 | Void Dancer | Slough triggers | Medium | Low |
| 7 | Closer | Positional ties | Medium | Low |
| 8 | Slow Burn | Held-card endgame | Medium | Medium |
| 9 | Conduit | Passing | Medium | Medium |
| 10 | Kingmaker | Empower partner | Fast | Medium |
| 11 | Contractor | Multiplied bids | Fast | High |
| 12 | Sandbagger | Bags as income | Slow | Low |
| 13 | Merchant | Triggered points | Slow → fast | Low |
| 14 | Spoiler | Set opponents | Timeout | Medium |
| 15 | Bag Bomber | Opponent bag penalty | Timeout | Low |
| 16 | Lawgiver | Global rule changes | Varies | High |

## Example Sigil Coverage

How the twelve example sigils map onto archetypes.

| Sigil | Serves |
|-------|--------|
| `#1` +10 rank | Crown, Trump Lord |
| `#2` +5 rank | Crown, Monosuit |
| `#3` −5 rank | Ghost, Bag Bomber |
| `#4` −10 rank | Ghost, All In |
| `#5` Becomes ace | Crown, Closer |
| `#6` Becomes king | Crown, Closer |
| `#7` Affinity low spots → face | Crown (consistency) |
| `#8` Affinity face → low spot | Ghost (consistency) |
| `#9` Non-spade → spade | Trump Lord, Void Dancer |
| `#10` Non-diamond → diamond | Monosuit, Void Dancer |
| `#11` Two → diamonds | Monosuit, Void Dancer |
| `#12` Adjacent +2 rank | Crown, Monosuit |

Gaps: the example list has no payoffs, no bid-time or round-start reveals, and no
passing, bag, or partner effects. Archetypes 6 and 8–16 need new sigils in those
categories.

## Open Questions

- **Passed sigil ownership.** When a sigil moves to another player, does "you"
  in its text mean the original owner or the new holder? Conduit's cursed-card
  play depends on the answer.
- **Starting collection.** Does a run start with any sigils? A starter sigil could
  seed an archetype and make round 1 less random.
- **Opponent archetypes.** Should AI opponents follow these same archetypes, so
  the scouting screen tells a readable story?
