# Rogue Spades: game rules and consolidated archetypes

Rogue Spades is partnership Spades with a persistent collection of **sigils** that changes what a freshly dealt hand can do. Win tricks to make your bid, earn partnership points, and use individual gold to buy sigils between rounds. Your collection persists through the run; the cards carrying it change every round.

This document consolidates [Deck Archetypes](deck_archetypes.md) and [deck archetypes](deck-archetypes.md). It preserves their distinct strategies under **22 archetypes**, merging alternate names where they describe the same plan. Each archetype includes two illustrative sigils.

**Status:** explicitly agreed rules take precedence over either draft. Sections labeled **proposed** supply recommendations where the drafts disagree or leave a gap; they are not additional user-approved rules. All named sigils and their numerical values are proposals for playtesting, not a finalized content list.

## 1. The table, the run, and victory

Four seats form two partnerships, with partners sitting opposite one another. A round uses a fresh standard 52-card deck, no jokers, and a 13-card hand for each seat. Players take turns clockwise. A **trick** is one card played by each of the four seats; a **round** comprises a deal, bidding, 13 tricks, and scoring. A **run** comprises up to 13 rounds. There is no separate encounter layer.

The game supports single-player and multiplayer with two or four human players. Opponents can have sigils. **Proposed mode default:** AI fills remaining seats, and two humans form one partnership; the precise two-human seating options remain a product decision. Do not assume that an AI partner must be sigil-less.

Partnership scores and bag counts start at zero and persist through the run. Scores can become negative; no additional negative-score elimination rule is assumed. Gold and sigil collections belong to individual players. The partnership wins by reaching **500 points**, or by having the higher score after **round 13** if neither side has reached 500.

**Proposed terminal procedure:** finish both partnerships' round scoring before checking victory. If either reaches 500, the higher-scoring partnership wins; if neither does, continue unless round 13 has ended. Equal scores at a terminal check produce a draw. This preserves the 13-round maximum and avoids awarding victory according to score-processing order. Terminal ties were not settled in the interview.

## 2. The lifecycle of a round

The following order is a **proposed timing framework** around the agreed deal, bidding, play, scoring, and shop loop.

1. **Prepare.** Before round one, each player can purchase one of three offered sigils. Later rounds use collections updated in the preceding shop. Select the first dealer randomly and rotate the dealer clockwise after each round.
2. **Scout.** If the proposed scouting feature is enabled, show all players' sigil collections without revealing the next deal or engraving locations. Resolve optional blind-nil commitments before showing any hand-dependent information.
3. **Deal and engrave.** Shuffle the standard deck, deal 13 cards to each seat, and assign each owned sigil to one card. Apply intrinsic rank and suit modifiers. Players inspect their hands; a blind-nil bidder's commitment is already locked.
4. **Before bidding.** Resolve effects explicitly scheduled before bidding, including global rules and pre-bid exchanges. Players can account for these changes in ordinary bids.
5. **Bid.** Starting left of the dealer, each player declares a bid in clockwise order. Ordinary bids are locked once declared unless a sigil explicitly permits a later adjustment.
6. **After bidding.** Resolve any enabled baseline nil exchange, then sigil-granted post-bid exchanges and start-of-play effects. These effects can change the hand or rules after players have committed.
7. **Play.** The player left of the dealer leads the first trick. Complete 13 tricks, resolving sigils in their stated windows. Between-trick exchanges occur before anyone plays to the next trick.
8. **Score and pay.** Calculate both partnership scores, including nils, bags, and sigil effects, then award individual gold. Check for the end of the run.
9. **Shop if continuing.** Each player may buy at most one of three offered sigils for the next round. Begin the next round with a fresh standard deal.

There is no strategically relevant shop after the run ends. A full 13-round run therefore offers **13 purchase opportunities**: one before round one and 12 between rounds. Skipping or being unable to afford a purchase can leave a player with fewer than 13 sigils.

## 3. Bids, legal plays, and trick winners

### Bidding

A positive bid is an integer from 1 to 13: the number of tricks the player expects to contribute. The two partners' positive bids form the partnership's **contract**. A partnership bidding three and four must take at least seven qualifying tricks to make its contract.

**Nil** is a separate promise to take no tricks, worth +100 if successful and −100 if the bidder takes any trick. Nil is not a bid to make zero partnership tricks: the other partner still has an ordinary contract. Both partners may bid nil, with each nil scored separately.

Blind nil and automatic exchanges on nil are variants proposed in one source, not consequences of simply saying “standard Spades.” Their optional rules appear in section 7.

### Following suit and trump

- The first card establishes the led suit. Each subsequent player must play that suit if they hold any card currently belonging to it.
- A player with no card of the led suit is **void** in that suit and may play any card. Playing current trump off suit is a **ruff**; playing a non-trump card off suit is a **slough**. Neither action requires the player to win the trick.
- Spades are normally trump. If any trump was played, only trump cards compete to win; otherwise only cards of the led suit compete. A high off-suit, non-trump card cannot win.
- Within the eligible suit, the highest effective rank wins. Equal effective ranks are won by the **latest card played**, including the third or fourth matching card.
- The winner takes the trick and leads the next one. A player cannot freely change seat order or choose another leader without an explicit sigil effect.
- Spades cannot normally be led until broken by an off-suit spade, unless the leader holds only spades. A suit conversion alone does not break spades; playing the resulting spade off suit does.

A player must follow suit even if this forces them to play an aura card, take an unwanted trick, or abandon an archetype's plan. There is no requirement to ruff when void or to overtake a card already winning.

### Rank and suit changes

Ranks are numeric: two through ten, jack 11, queen 12, king 13, ace 14. **The agreed ceiling is ace.** The proposed lower bound is two; one source treats it as settled, but it was not explicitly agreed in the interview. All example effects in this document use that proposed floor.

A converted card fully belongs to its new suit for following suit, trump, and breaking trump. Conversion and rank changes can produce duplicate suit/rank combinations; they do not add physical cards to the deck. A five changed into an ace of hearts ties a natural ace of hearts, so whichever eligible ace was played later wins.

**Proposed modifier convention:** evaluate a card's current base rank, including any explicit rank-setting effect, add active numerical modifiers, then clamp once to 2–14. If multiple effects set the base rank or suit, the latest resolved setter takes precedence. Removing an aura removes its modifier and recalculates the card. “+10” is not inherently more useful than “+5” if both reach ace.

Legality is checked when a card is played. A later effect changing a card already in the trick can change the winner but does not retroactively make the earlier play illegal. Such effects must explicitly say that they can target a played card.

## 4. Partnership scoring

For an ordinary contract, let **B** be the sum of positive bids and **T** the tricks eligible to satisfy those bids.

| Result | Ordinary contract score | New ordinary bags |
| --- | --- | --- |
| T ≥ B | 10 × B + (T − B) | T − B |
| T < B | −10 × B | 0 |

Add each nil's +100 or −100 separately. Accumulated bags carry across rounds; each group of ten costs 100 points, and the remainder carries forward. Apply any explicit sigil changes to contract value, bags, or bonus points as well.

**Proposed nil-trick convention:** tricks taken by a failed nil bidder do not help fulfill the positive contract and instead add bags. They do not also earn ordinary overtrick points. This makes nil handling explicit rather than relying on conflicting Spades variants. With two nil bidders, there is no positive contract; score both nils and count their taken tricks as bags.

**Proposed scoring order:** start with the +10 × B or −10 × B contract component; apply effects that specifically alter that component; add nil results, ordinary overtrick points, and sigil point bonuses; apply bag penalties. Count each component once. A contract multiplier does not multiply nil bonuses, bag penalties, overtrick points, or unrelated sigil rewards unless it explicitly says so. Effects that remove bags act before the round's bag-penalty check if their text specifies that timing.

### Worked examples

| Situation | Partnership's round score | Gold for each partner |
| --- | --- | --- |
| Bid 6, take 8, no bag threshold crossed | 60 + 2 = **62**; gain 2 bags | 62 |
| Bid 6, take 5 | **−60** | 0 |
| Successful nil, partner bids and takes 3 | 100 + 30 = **130** | 130 |
| Failed nil takes 1, partner bids and takes 3 | −100 + 30 = **−70**; gain 1 bag under the proposed convention | 0 |
| Enter with 8 bags, bid 5, take 8 | 50 + 3 − 100 = **−47**; carry 1 bag | 0 |
| Bid 4, take 4, earn 15 sigil bonus points | 40 + 15 = **55** | 55 |

A failed nil does **not** automatically imply zero gold: income depends on the final partnership total after every scoring component. For example, a failed nil and a made 11-trick contract score −100 + 110 = +10 before any other effects.

An average of roughly 39 points per round reaches 500 within 13 rounds, but it is a pacing reference, not a guarantee of victory: the opponents can reach 500 earlier or finish with more points. Denial builds can also win before round 13 if their own score reaches 500.

## 5. Gold, shops, and permanent progression

After each round, **each partner separately gains max(0, partnership round score) gold**. The award is copied into both wallets, not split. Negative scoring does not remove saved gold. Unspent gold persists within the run.

Sigils may explicitly grant personal bonus gold. **Proposed default:** award it to the controller identified when the effect triggers; do not also credit the partner. Bonus points increase partnership score and therefore both ordinary gold awards, while bonus gold alone does not increase points.

At a shop, buy at most one of three offered sigils or skip. Purchasing a sigil permanently adds it to that player's collection for the run. A collection has at most 13 sigils. No starting three-sigil package is assumed: the confirmed starting opportunity is one purchase from three offers.

Prices, starting gold, and offer probabilities need a balance table; the starting wallet should afford a starter offer. **Proposed optional shop features:** paid rerolls refresh the three offers without resetting the one-purchase limit; at the cap, a purchase may replace one owned sigil without refund. Neither feature was explicitly agreed. Multiple copies of a sigil are also a content decision, not implied by the one-per-card limit.

An income build is useful only if extra gold changes which sigil can be afforded or, with rerolls enabled, which offers can be found. Extra gold cannot buy a second sigil from the same shop. Economy cards bought too late to influence another meaningful purchase are usually poor investments.

## 6. Sigils and their rules

### Engraving and persistence

Every round, each owned sigil is engraved on one card in its owner's newly dealt hand. A card has **at most one engraving**. Affinity prefers a particular rank or suit when possible; remaining placements are random.

**Proposed placement procedure:** place affinity sigils first, randomizing order where they compete for eligible cards, then assign other sigils to remaining cards. Evaluate affinity against the fresh dealt cards before applying conversions. If no matching unengraved card remains, use a random unengraved card. No affinity promises a matching card on every deal.

One engraving per card does not prevent one sigil from affecting other cards. A while-held aura can strengthen cards engraved with different sigils, and a revealed scoring effect can reward unengraved cards. Engines must work across those separate cards rather than require multiple engravings on a single card.

Card changes, temporary effects, and transferred cards reset after the round. Purchased sigils return to their permanent owners' collections for the next deal. There is no permanent card acquisition or permanent conversion of the standard deck unless a future rule explicitly adds it.

### Effect types and timing

| Type | What it does | Example window |
| --- | --- | --- |
| Intrinsic card modifier | Changes the engraved card's rank or suit | After engraving, before inspection and bidding |
| Before-bidding reveal | Establishes information, a rule, or a preparation effect | Before ordinary bids |
| Bid reveal | Changes a bid or its eventual value | When its controller bids |
| Start-of-play reveal | Changes the round after commitments | After all bids and scheduled exchanges |
| While held | Applies only while the card remains in its controller's hand | Recalculated as the hand changes |
| When played | Resolves after a legal card is committed | Before trick resolution |
| Win or loss trigger | Rewards or reacts to the resolved outcome | After the trick winner is determined |
| Slough or ruff trigger | Responds to a legal off-suit play | At play, unless it also requires a win |
| Pass trigger | Responds to a specified exchange | After that exchange completes |

**Triggered** effects happen when their conditions occur. **Ongoing** effects continually modify applicable rules during their stated lifetime. Ongoing does not mean permanent across rounds: a while-held aura ends when played, whereas a “for this round” reveal survives its source card leaving the hand.

Additional conditions can reference the led suit, trick position, partnership bid status, remaining suit count, or another public event. Every sigil should specify its timing, target, controller, information revealed, and duration.

### Passing and control

Sigils may grant exchanges before bids, after bids, or during play. Exchanges use equal numbers of remaining cards so hand sizes stay aligned. **Proposed ordinary timing:** resolve in-play exchanges between completed tricks; an exchange after one seat has played to the next trick requires separately specified rules and is not assumed here.

Unless a sigil says otherwise, each participant selects the card they contribute. Selection does not give permission to inspect the other hand. A required exchange cannot occur when a participant lacks enough remaining cards.

**Proposed ownership model:** the engraving travels with the passed card. The new holder controls future card-bound effects; “you” means that controller, including for harmful effects. Permanent collection ownership does not change. An already-revealed round effect remains attached to the controller who revealed it, and an already-triggered reward keeps its recorded recipient. This resolves the source documents' open ownership question without making it a confirmed rule.

### Information and simultaneous effects

**Proposed information model:** your hand and its engraving locations are private. Other players see a sigil when it activates or explicitly reveals itself. Scouting makes collections public, not individual card assignments. Bids, played cards, trick counts, partnership scores, and bags are public. Public trigger resolution reveals enough information to understand its result.

Blind-nil bidders must commit before seeing their deal or any deal-dependent reveals. Public knowledge of collections is permitted; private inspection of an engraved hand is not.

**Proposed resolution convention:** resolve simultaneous effects in clockwise order, starting with the active player for a play event and left of the dealer for shared round windows. When one player controls several simultaneous effects, they choose their order. Complete the current event before checking the next event. Resolve each trigger once per event; do not permit unbounded pass-trigger chains.

Global rule setters that conflict on the same property use the latest resolved setter; setters for different properties can coexist. A sigil replacing trump must say whether it also changes lead restrictions and ruff/slough classification. “Lowest wins” reverses rank comparison within the eligible suit; it does not let an off-suit non-trump card win. Tied eligible ranks still favor the later card.

Adjacency effects require a defined hand order. **Proposed default:** establish fixed slots at the deal, keep them through the round, leave empty slots when cards are played, and place exchanged cards in vacated slots. Visual sorting does not change mechanical adjacency. This prevents free dragging from silently becoming an unlimited retargeting ability.

## 7. Optional nil variants retained from the earlier draft

These proposals are included so that All In and the original passing concepts are not lost, but they are not baseline requirements for the other archetypes.

- **Blind nil:** before inspecting the hand or any deal-dependent information, commit to taking zero tricks for +200 on success or −200 on failure. Ordinary partner scoring remains separate. Proposed eligibility has no deficit requirement; any restriction would need an explicit rule.
- **Baseline nil exchange:** after all bids lock, a partnership containing at least one nil or blind-nil bidder simultaneously exchanges two cards, each partner choosing their outgoing cards before seeing the incoming cards. Use one exchange per partnership, even if both bid nil. These exchanges do not require a sigil.
- **Sigil-granted passing remains independent:** with or without the baseline nil-exchange option, a sigil can allow ordinary bidders to exchange and can grant additional timing windows or different recipients.

All In depends on enabling blind nil. Ghost, Bodyguard, and Relay can function without baseline nil passing by purchasing suitable sigils.

## 8. Consolidated archetypes

An archetype describes how the player helps win the **partnership score race**. It is not a promise to make the same bid every deal. A useful collection has enablers, payoffs, and enough consistency to survive random engraving.

Each entry below gives **two example sigils**. Numerical rewards are initial playtest values; no sample pair is intended as a complete build. Rank changes use the proposed 2–14 limits. Point rewards settle at round end. A sigil revealed “for this round” remains active after its source card is played.

### 1. Ghost — avoid every trick

**Also called:** Ghost Hand. **Win plan:** repeatedly make nil while the partner completes an ordinary contract. Choose nil based on the actual hand rather than treating every deal as safe.

- **Diminish — intrinsic; affinity face cards:** reduce this card's rank by ten.
- **Plain Clothes — intrinsic; affinity spades:** this card becomes the two of hearts.

The combination addresses both high ranks and dangerous trump. Low-card ties still favor the later player, so even a hand full of twos is not guaranteed safe. Partner coverage and exchanges are useful support; opponents attack short suits and compulsory winners.

### 2. All In — commit to blind nil

**Status:** requires the optional blind-nil rule. **Win plan:** earn the larger ±200 result by buying effects that make an unseen deal safer, accepting substantially higher variance than Ghost.

- **Veil — before bidding, after inspection; requires your locked blind nil:** reveal for this round; your non-spades have −5 rank.
- **Emergency Parcel — after bids lock; requires your blind nil:** exchange up to two cards with your partner, who selects the same number of cards to return.

These effects activate after the blind commitment and do not permit peeking. Neither guarantees a safe hand; opponents can still force low trumps or tied low cards to win. Additional nil bonuses should be especially restrained.

### 3. Crown Court — make large contracts with high cards

**Also called:** Crown. **Win plan:** build reliable winners across suits, bid ambitiously, and cash them before opponents can ruff.

- **Coronation — intrinsic:** this card becomes an ace.
- **Promotion — intrinsic; affinity low spots, defined here as ranks 2–9:** increase this card's rank by five.

Upgrades have diminishing returns at ace. Later tied aces and trump still beat apparent winners, so the build needs suit coverage and measured bidding rather than rank alone.

### 4. Spade Flood — dominate the trump reserve

**Also called:** Trump Lord. **Win plan:** create enough spades to outlast opposing trump, then take the remaining tricks for a large contract.

- **Black Banner — intrinsic; affinity non-spades:** this card becomes a spade.
- **Trump Captain — while held:** your other spades have +2 rank.

Quantity and strength are different needs. Opponents with stronger trump can punish a flood of small spades, and a nearly all-spade hand still has to obey leading restrictions. Excess compulsory winners can become bags.

### 5. Monosuit — establish a long side suit

**Win plan:** concentrate a non-trump suit, exhaust its opposing cards and relevant trump, then win late tricks through suit length. This is different from scoring merely for playing hearts.

- **Diamondward — before bidding:** reveal; two other random non-diamonds in your hand become diamonds.
- **Standard Bearer — while held; affinity diamonds:** your other diamonds have +2 rank.

A partner who draws trump helps the long suit survive. Concentration also makes opponents void, creating ruff opportunities for them. Anti-ruff global effects are an advanced proposal, not an inherent property of a long suit.

### 6. Slough Engine — turn off-suit discards into score

**Also called:** Void Dancer. **Win plan:** create a void, then earn points by discarding non-trump cards while maintaining a modest contract.

- **Suit Consolidation — before bidding; affinity diamonds:** reveal; one other random diamond in your hand becomes a heart, if one exists.
- **Open Channel — start of play:** reveal for this round; your first three legal sloughs each award your partnership 5 points.

A ruff is not a slough, even when it loses. The build wants repeated off-suit discard opportunities, not merely losing cards. Opponents can lead suits still held to deny the engine.

### 7. Last Word — win the tie from a later seat

**Also called:** Closer. **Win plan:** make selected contract tricks more reliable by matching a winning rank after the opponent commits it.

- **Echo Crown — when played:** if an ace of this card's suit is already in the trick, this card becomes an ace.
- **Courtesy — when played:** you may reduce this card's rank by five.

Courtesy can help surrender the lead; Echo Crown exploits a later position on a future trick. Neither reorders the seats. The player must still follow suit, and a subsequent matching ace can overtake theirs.

### 8. Slow Burn — save a stronger finish

**Win plan:** retain cards whose power grows or benefits the hand while held, concede selected early tricks, and take enough late tricks to make the bid.

- **Patience — while held:** after each completed trick, this card gains +1 rank for the round, up to +5 total.
- **Reserve Captain — while held:** your other cards of this card's suit have +2 rank.

The player cannot be void in a suit while holding a card of that suit. Instead, retain other followers that can be spent first, or use exchanges to avoid being forced to play the reserve early. No endgame is guaranteed against ruffs, later ties, or forced leads.

### 9. Relay — allocate cards between hands

**Also called:** Conduit. **Win plan:** turn two uneven hands into complementary ones through timely exchanges, moving winners toward trick bids and danger away from nil.

- **Opening Relay — before bidding:** exchange this card for a card selected by your partner.
- **Late Delivery — once between tricks while held:** exchange this card for a card selected by your partner.

Passing is not restricted to nil when a sigil grants it. Exchanges move engravings under the proposed control model, but do not move permanent collection ownership. Bad timing can remove essential coverage or contradict an already-locked bid.

### 10. Kingmaker — strengthen the partner's contract

**Win plan:** bid modestly and use your plays to make the partner's hand stronger. Partnership points care about the combined successful contract, not which non-nil partner supplied every trick.

- **Royal Gift — when this card loses:** your partner chooses one remaining card in their hand to gain +3 rank for the round.
- **Shared Standard — while held:** your partner's cards matching this card's suit have +2 rank.

This build works with a partner who can turn buffs into useful tricks. It can actively harm a nil-bidding partner by creating winners, so it is not automatically a Ghost pairing. Supporting an AI partner does not require that partner to begin without sigils.

### 11. Contractor — increase what a bid is worth

**Win plan:** use bid-time effects to earn more points from a manageable contract. Its central resource is contract value, rather than merely controlling overtricks.

- **Bonded Contract — when you make a positive bid:** reveal; if your partnership makes its contract, add 3 points per trick you personally bid, up to 15; if set, subtract the same amount.
- **Fine Print — after the first trick; requires your positive bid:** reveal; you may change your bid by one, keeping it between 1 and 13; update the partnership contract immediately.

The earlier draft's doubled bids and +50 exact-contract rewards remain more aggressive balance variants, not default values. Extra bid value and post-bid adjustment must not remove the risk of being set.

### 12. Sandbagger — make your own overtricks profitable

**Win plan:** underbid selectively, then earn enough from surplus tricks or bag relief to outperform an honest larger bid. Without a payoff, deliberately collecting bags is usually costly.

- **Overflow — when you bid:** reveal for this round; your partnership's first three ordinary overtricks each award 4 extra points.
- **Amnesty — after play, before bag penalties:** reveal; if your partnership made its contract, remove up to two accumulated bags; do not remove the ordinary points already earned by those overtricks.

The player still weighs the next bag threshold and the value lost by bidding too low. Bag relief and bonus scoring need shared-copy limits; otherwise several copies can erase the underlying tradeoff.

### 13. Merchant — score through a broad trigger package

**Win plan:** add enough event-based points to an achievable contract to win the score race. This is a broad payoff strategy, while Heart Chorus, Graceful Defeat, and Slough Engine specialize in particular events.

- **Bounty — when this card wins a trick:** award your partnership 5 points.
- **Appearance Fee — when played to a heart-led trick:** award your partnership 3 points, whether or not this card wins.

Trigger count matters, but abandoning a 40-point contract to earn a 3-point bonus is usually a losing trade. Bonus points also fund both partners. Direct gold belongs to the separate Investor plan and is not interchangeable with score.

### 14. Siege — set the opponents

**Also called:** Spoiler. **Win plan:** make a safe contract while denying the opponents a necessary winner or breaking their nil. The score swing can beat merely collecting more overtricks.

- **Breach — when played:** reduce one opponent's card already in this trick by five ranks for this trick.
- **Reconnaissance — after bids lock:** each opponent reveals one spade of their choice from their hand, if they have one.

Information helps identify the decisive attack. Reducing a trump's rank does not make it lose to a non-trump ace. Cautious opposing bids reduce denial opportunities, and setting both sides may fail to improve the score race.

### 15. Bag Trap — make opponents take too many

**Also called:** Bag Bomber. **Win plan:** fulfill your own bid, then feed the opponents enough surplus tricks to trigger their accumulated-bag penalty.

- **Poisoned Gift — after bids lock:** exchange this card for a card selected by one opponent you choose.
- **Bag Bomb — when this card loses to an opponent:** if that partnership has already fulfilled its positive contract, add one extra bag to its counter, with no extra point.

Gift is useful when it hands over an awkward winner; it is not automatically beneficial. Bag Bomb is an explicit exception that creates a bag beyond ordinary overtricks. A set and a bag penalty demand opposite trick-taking plans, so Siege and Bag Trap are situational alternatives rather than always-complementary engines.

### 16. Lawgiver — make the round favor your collection

**Win plan:** use announced rule changes that favor your hand or punish opponents' locked commitments. The rule itself is an enabler; the actual scoring route is still contracts, denial, or trigger rewards.

- **Low Court — before bidding:** reveal for this round; the lowest rank wins within the eligible suit, with normal suit priority and later-card tie resolution.
- **Treaty — start of play, after bids lock:** reveal for this round; there is no trump and no restriction on leading spades; only the led suit can win.

Low Court is visible before ordinary bids; Treaty intentionally changes conditions afterward. Under Treaty, off-suit plays are sloughs and no play is a ruff. “Lowest wins” can destroy an existing nil plan; it is not automatic synergy with rank reduction. Competing global setters use the proposed precedence rules in section 6.

### 17. Bodyguard — protect the partner's nil

**Win plan:** use your winners and exchanges to keep the nil bidder from taking a trick, while making the partnership's positive contract. The 100-point nil payoff justifies protection.

- **Rescue Exchange — after bids lock:** exchange this card for a card selected by your nil-bidding partner.
- **Cover — when played after your nil-bidding partner:** if this card has the same suit as their card in the trick, this card becomes an ace.

Cover still requires a legal play and can be beaten by trump or a later matching ace. Unlike Kingmaker, this build wants the partner's hand to remain weak and keeps the covering strength in its own hand.

### 18. Needle — ruff the tricks that matter

**Win plan:** engineer a useful void and spend a small trump reserve on decisive steals, rather than trying to own the most spades.

- **Evacuation — before bidding:** exchange this card for a partner-selected card of a different suit, if one is available.
- **Ambush — when this card is legally played as a ruff:** increase its rank by five for this trick.

The best ruff takes an opponent's essential winner, not a trick the partner already controls. Opponents can draw out the small reserve with trump leads or overruff it. Void creation must target the actual dealt hand.

### 19. Heart Chorus — make hearts a scoring engine

**Win plan:** create heart density and score from repeated heart participation, while retaining enough ordinary strength to fulfill the bid. Hearts have no innate bonus outside the sigils.

- **Heartward — before bidding:** reveal; two other random non-hearts in your hand become hearts.
- **Chorus — start of play:** reveal for this round; the first three hearts you play each award your partnership 5 points.

Unlike Monosuit, the payoff does not require those hearts to win after trump is exhausted. Unlike Merchant, the collection is deliberately built around one suit. Opponents can force other suits, ruff valuable hearts, and attack the ordinary contract.

### 20. Diamond Investor — turn early gold into later strength

**Win plan:** earn personal bonus gold early, then buy more effective scoring sigils before the opponent reaches 500 or the round limit arrives. Diamonds are a proposed theme, not a baseline income rule.

- **Diamondward — before bidding:** reveal; two other random non-diamonds in your hand become diamonds.
- **Dividend — start of play:** reveal for this round; the first three diamonds you play each grant you 5 personal gold after the round.

The converter also serves Monosuit, but the Investor's objective is purchasing power. If all desired purchases are already affordable and rerolls are unavailable, the extra income has little purpose. A late economy purchase can waste the last meaningful shop.

### 21. Exact Contract — make the bid and stop

**Win plan:** score reliably while avoiding bag penalties, with optional bonuses for exactness. This is card-control strategy, distinct from Contractor's changes to bid value.

- **Measured Step — when played:** choose to increase or decrease this card's rank by five for this trick.
- **Clean Ledger — when you make a positive bid:** reveal; if your partnership makes its contract with no new bags this round, add 10 points.

Both partners need to track the remaining required tricks. Ducking too early can turn a cheap bag into an expensive set, while an opponent can force a surplus winner after the contract is complete.

### 22. Graceful Defeat — make selected losses valuable

**Win plan:** retain enough winners for a modest contract and use the remaining cards to earn points by losing. Unlike Ghost, the player expects to take some tricks; unlike Slough Engine, no void is required.

- **Consolation — when this card loses a trick:** award your partnership 4 points, including if your partner won.
- **Honorable Loss — when this card follows suit and loses to an opponent:** award your partnership 6 points.

Different recipient conditions create different incentives. Opponents can duck the reward card or deny necessary contract tricks. Losing a required trick for a small reward is still a bad exchange.

## 9. What was merged, retained, or corrected

| Earlier names or claims | Consolidated treatment |
| --- | --- |
| Ghost / Ghost Hand | Ghost |
| Crown / Crown Court | Crown Court |
| Trump Lord / Spade Flood | Spade Flood |
| Void Dancer / Slough Engine | Slough Engine |
| Closer / Last Word | Last Word |
| Conduit / Relay | Relay |
| Spoiler / Siege | Siege; not limited to winning at the round cap |
| Bag Bomber / Bag Trap | Bag Trap; ordinary trick steering and explicit extra-bag effects are separate tools |
| Contractor / Exact Contract | Retained separately: alter contract value versus control trick count |
| Kingmaker / Bodyguard | Retained separately: strengthen a trick-taking partner versus protect a nil partner |
| Monosuit / Heart Chorus | Retained separately: win through established suit length versus earn suit-trigger points |
| Merchant / Diamond Investor | Retained separately: bonus score versus personal purchasing power |
| All In, Slow Burn, Sandbagger, Lawgiver | Retained from the underscore-named document |
| Needle, Graceful Defeat | Retained from the hyphen-named document |
| Uncertain starting collection; roughly 12 purchases | Confirmed pre-round-one shop; up to 13 useful purchase opportunities |
| Only nil bidders pass | Proposed baseline nil exchange; sigils can also grant passing to other bidders |
| Blind nil, rerolls, public scouting presented as rules | Retained as proposals, not interview-confirmed baseline rules |
| Ranks always clamped at two | Proposed floor; only the ace ceiling was explicitly confirmed |
| Failed nil always means no income | Gold is based on the final partnership round total |
| Stay void in the held card's suit | Impossible while that card is held; retain alternative followers or use exchanges |
| Every archetype has a known speed or variance | Treat these as playtest hypotheses, not established balance results |

Suit-changing and rank-changing sigils from the initial examples remain broadly useful enablers. Affinity improves their consistency; adjacent +2 bonuses can support Crown Court or Monosuit under a defined hand-ordering rule. Passing, bid-value, loss, bag, partner-support, and global-rule archetypes require effects beyond that initial modifier list.

## 10. Balance priorities and decisions still requiring approval

The major unresolved rules have concrete recommendations above: a two-rank floor; draws on terminal ties; failed-nil tricks as bags rather than contract help; explicit effect and ownership ordering; and fixed mechanical adjacency. Blind nil, baseline nil exchanges, rerolls, scouting, replacement, and duplicate availability remain feature choices. Starting gold and prices still need numerical tuning.

Playtesting should prioritize these interactions:

- **Score funds more score:** point bonuses both advance victory and finance both partners, so their impact exceeds the printed point value.
- **Nil acceleration:** successful nil already supplies a large payout; blind nil and loss bonuses can shorten the run before slower builds repay their cost.
- **One purchase per shop:** economy must improve affordability or offer access rather than depend on buying more sigils at once.
- **Copies and global effects:** repeated reward, bag-removal, and bid-value effects need explicit stacking limits; one engraving per card does not prevent excessive stacking across a hand.
- **Archetype identity:** high ranks, trump quantity, selective ruffs, suit length, and positional ties should lead to meaningfully different choices.
- **Counterplay and fallback:** every build needs a credible ordinary bid when its deal, engraving, or shop offers do not support the ideal plan.
- **Partner compatibility:** nil protection, rank buffs, and coordinated passing must account for the partner's actual bid rather than assume every support effect helps.
- **Information:** post-bid global changes should be threatening without making informed bidding irrelevant; public collection scouting is one proposed source of warning.

The target is a game where players can explain how their collection intends to win, recognize the opposing plan, and adapt to the hand actually dealt.
