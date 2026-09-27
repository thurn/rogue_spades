# Rogue Spades deck archetypes

A deck archetype answers **“How is this player going to help their partnership win the run?”** It is a plan for converting a changing hand into partnership points, supported by a persistent collection of sigils. It is not merely a favorite suit or a collection of individually powerful effects.

This document proposes **14 archetypes**. Their sigils are design examples, not an approved card list or final balance values. The archetypes should guide sigil design, shop offerings, and playtesting without requiring every collection to fit a single label.

## Established rules

- Four seats play in two partnerships under standard Spades rules, with sigils providing explicit exceptions; multiplayer supports two or four human players, and opponents can have sigils too.
- A partnership wins by reaching 500 points, or by having the higher score after 13 rounds. There are no separate encounters within a run.
- Standard scoring applies: a made partnership bid scores ten times the bid plus one per overtrick; a failed bid loses ten times the bid. Nil adds or subtracts 100 points, and every ten accumulated bags costs 100 points.
- Gold is individual. Each partner receives gold equal to the partnership's total round score, floored at zero. A +130 round grants each partner 130 gold; a negative round grants neither gold and does not remove saved gold.
- A player can buy one of three offered sigils before round one, and shops after subsequent rounds offer one of three sigils to purchase for future rounds.
- Each owned sigil engraves one card each round. Assignment is randomized again with each fresh hand, with affinity guiding placement when possible.
- A card can hold at most one sigil, and a player can own at most 13 sigils. An engine must work across separate engraved cards; it cannot depend on stacking several sigils on one card.
- A fresh standard deal starts each round. Changes to card rank, card suit, and card ownership do not persist into the next round; purchased sigils do.
- Modified ranks cannot exceed ace. Between cards tied for winning strength, the later card wins, including when a third or fourth card ties. Suit eligibility and trump take precedence over rank.
- Sigils can pass cards after bidding and during trick play. The agreed design direction uses equal-size exchanges, with timing specified by the sigil, to preserve hand sizes.

The examples below preserve following suit, normal trump eligibility, and the normal constraints on leading unbroken spades unless their text explicitly provides an exception. Losing a card deliberately does not grant permission to revoke.

## What makes a viable archetype

An archetype needs a scoring route, a way to function with random engraving, and decisions that remain interesting against opponents with sigils. A partner role describes how the two hands cooperate, not a requirement that both humans select matching builds.

There are three main scoring routes:

1. **Make valuable contracts:** increase the partnership's reliable tricks, protect nils, or improve control over the final trick count.
2. **Damage opposing contracts:** set the opponents, break their nil, or drive them into a bag penalty.
3. **Earn extra value:** gain points or gold through sigils, then turn that advantage into a winning score before the run ends.

Gold is not a victory condition. Ordinary scoring already funds both partners, so an economy archetype needs a concrete advantage over simply scoring well. Its investment horizon can be much shorter than 13 rounds when a partnership approaches 500.

### Archetype map

| # | Archetype | Primary route to victory | Distinctive resource or decision |
| --- | --- | --- | --- |
| 1 | Crown Court | Make large bids with strong cards across suits | Reliable side-suit winners |
| 2 | Ghost Hand | Repeatedly make nil | Safe exits and rank suppression |
| 3 | Bodyguard | Convert a partner's risky nil into a dependable 100 points | Coverage and coordinated exchanges |
| 4 | Spade Flood | Make large bids through trump superiority | Trump quantity and exhaustion |
| 5 | Needle | Steal selected tricks with a small trump reserve | Voids and timing |
| 6 | Heart Chorus | Add points through repeated heart participation | Suit density and shared rewards |
| 7 | Diamond Investor | Buy stronger scoring tools earlier | Gold acceleration and payback time |
| 8 | Relay | Assemble two coherent hands through exchanges | Card allocation and information |
| 9 | Exact Contract | Preserve contracts while minimizing costly bags | Switching between taking and ducking |
| 10 | Last Word | Win capped-rank contests by acting later | Lead ownership and trick position |
| 11 | Siege | Set the opposing partnership | Denial of essential tricks |
| 12 | Bag Trap | Convert opposing overtricks into a 100-point penalty | Opponent bag count and forced winners |
| 13 | Graceful Defeat | Score from selected losses while making a modest bid | Losing eligible cards profitably |
| 14 | Slough Engine | Turn legal off-suit discards into points and hand improvement | Voids and expendable cards |

## 1. Crown Court — make the big bid

**Win plan.** Build a hand with enough dependable winners across several suits to bid aggressively and collect large contract payouts. This is the straightforward high-rank archetype, but an ace is not an unconditional winner: it can be ruffed or beaten by a later ace.

**Engine and proposed sigils.**

- **Coronation:** this card becomes an ace.
- **Promotion:** affinity for low spots; increase this card's rank by five, capped at ace.
- **Royal Household:** while held, other cards in your hand of this card's suit have +2 rank, capped at ace.

The support effect improves different cards rather than engraving them a second time. Affinity keeps upgrades away from cards that already reach the ceiling.

**Play and partner role.** Count winners conservatively, cash side-suit strength before opponents become void, and preserve an entry to regain the lead. A partner who handles weak suits or supplies a few reliable trumps makes the contract less dependent on one hand.

**Shop priorities and counters.** Buy efficient upgrades and coverage before redundant ace makers. Opposing trump builds, later tied aces, and rank suppression punish overbidding. Extra +10 effects have little value on cards that already cap at ace.

**Why it is distinct.** It increases the number of naturally winning cards across suits, rather than concentrating on trump or earning rewards for particular events.

## 2. Ghost Hand — make nil a repeatable plan

**Win plan.** Earn the 100-point nil bonus repeatedly while the partner makes the partnership's ordinary contract. Successful nil contributes gold through the same score-based payout as other scoring routes.

**Engine and proposed sigils.**

- **Diminish:** affinity for face cards; reduce this card's rank by ten.
- **Plain Clothes:** affinity for spades; this card becomes a low heart.
- **Quiet Exchange:** before bidding, exchange this card for a card chosen by your partner.

These effects remove different kinds of danger: high rank, unavoidable trump, and a single exposed winner. A low spade can still accidentally win, so rank reduction alone is insufficient.

**Play and partner role.** Inspect the actual engraving before committing to nil, shed dangerous cards under cover, and preserve low cards in suits opponents can force. The partner bids for their own expected tricks and protects the nil where possible.

**Shop priorities and counters.** Prefer effects that consistently target dangerous cards. A bad deal still warrants a normal bid. Opponents can repeatedly lead a short suit, exhaust safe exits, or use exchanges to introduce a winner after bids lock.

**Why it is distinct.** Its desired personal trick count is zero; collecting more winners can actively damage its scoring engine.

## 3. Bodyguard — make the partner's nil safe

**Win plan.** Specialize in winning the tricks that would otherwise break a partner's nil, while fulfilling the non-nil side of the contract. The payoff is the partner's 100-point bonus, not a separate protection reward.

**Engine and proposed sigils.**

- **Rescue Exchange:** once after bids lock, before a trick begins, exchange this card for a card selected by your partner.
- **Cover:** when played after a nil-bidding partner, if this card has the same suit as their card, it becomes an ace.
- **Shelter:** before bidding, reveal this card; your partner may reveal one card to you to help plan coverage.

Cover does not allow an illegal play or guarantee the trick against trump or another later ace. Exchanges and information help the player find legal opportunities to protect the partner.

**Play and partner role.** Keep coverage in the partner's dangerous suits and take responsibility for cards that threaten nil. The partner needs some capacity to avoid tricks, but need not own a complete Ghost Hand collection.

**Shop priorities and counters.** Prioritize breadth of coverage and timely exchanges. The build loses value when no safe nil is available, so it needs enough ordinary strength to play a normal contract. Opponents attack uncovered suits and exploit unfavorable seating order.

**Why it is distinct.** Ghost Hand removes its own winners; Bodyguard retains winners and allocates them to protect someone else.

## 4. Spade Flood — outlast every other trump hand

**Win plan.** Create enough spades to exhaust opposing trump, then collect tricks with the remaining reserve and make a large bid.

**Engine and proposed sigils.**

- **Black Banner:** affinity for non-spades; this card becomes a spade.
- **Recruitment:** before bidding, reveal this card; one other random non-spade in your hand becomes a spade.
- **Trump Captain:** while held, your other spades have +2 rank, capped at ace.

Suit conversion changes the dealt suit distribution for this round only. Multiple conversions build density across separate cards.

**Play and partner role.** Decide whether to draw trump or preserve it for ruffs. Count opposing spades and avoid wasting the entire reserve on a fight the opponents can win. The partner can cash side-suit winners while opponents still have to follow suit.

**Shop priorities and counters.** Buy both density and enough strength to avoid losing the trump war. Trump concentration can leave a hand full of compulsory winners, expose a bid to stronger spades, or generate bags after the contract is made.

**Why it is distinct.** The resource is sustained trump superiority, not simply a few well-timed ruffs.

## 5. Needle — steal the expensive tricks

**Win plan.** Create a useful void and use a small number of trumps to take tricks the opponents were relying on. Combine those steals with a modest, reliable contract.

**Engine and proposed sigils.**

- **Evacuation:** before bidding, exchange this card for a partner-selected card of another suit, if available.
- **Narrow Wardrobe:** affinity for diamonds; this card becomes a heart.
- **Ambush:** when this card is legally played as a ruff, increase its rank by five, capped at ace.

The conversion and exchange package aims to remove the final cards of a suit; indiscriminate conversion is less useful than completing a void.

**Play and partner role.** Preserve trump for vulnerable opposing winners, avoid ruffing a trick the partner already controls, and account for overruffs. The partner can lead into a known void when doing so helps the partnership.

**Shop priorities and counters.** Prioritize void creation and selective trump strength. Opponents can lead spades to strip the reserve, avoid the void suit, or overruff. A long trump fight favors Spade Flood instead.

**Why it is distinct.** It wins through efficient use of scarce trump rather than maximizing trump quantity.

## 6. Heart Chorus — turn suit density into score

**Win plan.** Create many hearts and earn bounded bonus points by playing them, while retaining enough trick-taking ability to make the partnership bid. Hearts have no inherent special scoring rule; proposed sigils give them one.

**Engine and proposed sigils.**

- **Heartward:** before bidding, reveal this card; two other random non-hearts in your hand become hearts.
- **Chorus:** reveal at the start of play; the first three tricks this round containing a heart you played each award your partnership a small bonus at round end.
- **Refrain:** if this heart wins a trick containing another heart, award a small additional round-end point bonus.

The shared reward can see hearts on other cards, so the converter and payoff do not need to occupy the same card. Chorus rewards participation; Refrain provides a reason to retain some strong hearts.

**Play and partner role.** Choose when to lead hearts, when to cash a strong heart, and when a low heart can earn its reward safely. The partner supplies coverage outside the concentrated suit.

**Shop priorities and counters.** Find a payoff before investing heavily in conversion. Opponents can ruff hearts or keep leading suits that strand them in hand. Bonus points must not make a routinely failed contract profitable by default.

**Why it is distinct.** Suit density itself unlocks scoring opportunities; it is not just a high-rank hand recolored red.

## 7. Diamond Investor — buy a scoring advantage early

**Win plan.** Earn extra personal gold early, purchase better scoring tools sooner, and finish with a stronger collection. Diamonds are a proposed economic identity, not an established rule.

**Engine and proposed sigils.**

- **Diamondward:** before bidding, reveal this card; two other random non-diamonds in your hand become diamonds.
- **Dividend:** reveal at the start of play; the first three diamonds you play each grant you a small amount of bonus gold after the round.
- **Frugal Mark:** when this card wins a trick, earn a discount on your next purchase, usable once and without reducing the price below zero.

Direct gold rewards go to the sigil owner. They are proposed exceptions to the ordinary score-based income rule and do not automatically grant gold to the partner.

**Play and partner role.** Maintain a respectable bid while collecting the bonus. The partner benefits when the investor uses better sigils to increase future partnership scores; they do not receive the investor's wallet.

**Shop priorities and counters.** Buy acceleration early, then buy a scoring engine such as Crown Court or Heart Chorus. Do not buy late income with no useful shop remaining. If normal score income already buys every desired offer, or if extra gold cannot improve the one permitted purchase, this archetype has no economic purpose and needs redesign.

**Why it is distinct.** It accepts a short-term opportunity cost for future buying power. The one-purchase limit means money must improve purchase quality or affordability, not purchase count.

## 8. Relay — put each card in the right hand

**Win plan.** Use exchanges to assemble complementary hands: move winners to the partner bidding for tricks, dangerous cards away from nil, and suit fragments out of a hand that benefits from a void.

**Engine and proposed sigils.**

- **Opening Relay:** before bidding, exchange this card for a card selected by your partner.
- **Late Delivery:** once after bidding and before a trick begins, offer this card to your partner in exchange for a card they select.
- **Return Address:** when played, arrange a one-card exchange between partners before the next trick, with each partner selecting a card from their remaining hand.

Each exchange is equal-size. An exchange cannot occur after one participant has already played to the next trick, and no exchange occurs if a required hand is empty.

**Play and partner role.** Plan the partnership's two hands together, but distinguish pre-bid optimization from post-bid rescue. A later exchange must still serve the contract already made. Both partners gain from knowing what role the other is trying to play.

**Shop priorities and counters.** Value selective exchanges and useful timing over raw exchange count. Badly timed passing can transfer a problem without solving it, strand a winning card, or remove needed coverage. Information available to opponents and to the partner is part of each sigil's design.

**Why it is distinct.** It improves allocation rather than creating raw card strength. Its best recipient can change from round to round.

## 9. Exact Contract — take enough, then stop

**Win plan.** Make the partnership bid consistently while avoiding bag penalties over the run. Ordinary Spades gives no bonus for exactness; the baseline payoff is reliability and fewer penalties.

**Engine and proposed sigils.**

- **Measured Step:** when played, choose to increase or decrease this card's rank by five, respecting the rank ceiling.
- **Brake:** while held, after your partnership reaches its bid, your other non-spades have reduced rank.
- **Clean Ledger:** if your partnership makes its bid with no overtricks, add a small round-end point bonus.

Measured Step must be declared before resolving the trick. Brake affects remaining opportunities; it cannot undo tricks already won.

**Play and partner role.** Track the combined trick count, identify which hand can safely take the remaining required tricks, and retain cards that can duck afterward. A partner who can follow the same plan helps avoid competing attempts to finish the contract.

**Shop priorities and counters.** Favor flexibility over permanent rank reduction. Over-correcting can turn a small bag cost into a much larger set. Opponents can force unavoidable winners or deny the final required trick.

**Why it is distinct.** It optimizes the stopping point, not the maximum number of tricks. Flexible cards remain useful both before and after the bid is met.

## 10. Last Word — make position beat strength

**Win plan.** Exploit the rank ceiling and the rule that the later tied card wins. Arrange to play matching aces after the opponent's apparent winners, converting positional opportunities into contract tricks or sets.

**Engine and proposed sigils.**

- **Echo Crown:** when played, if an ace of this card's suit has already been played to this trick, this card becomes an ace.
- **Courtesy:** decrease this card's rank when played, helping surrender the lead legally.
- **Private Signal:** before a trick begins, reveal this card to your partner so they can plan around your potential winner.

Echo Crown still loses to a winning trump when it is not itself trump. Acting second is not enough if a later opponent can tie again.

**Play and partner role.** Infer who will lead the next trick, preserve followers that can become matching aces, and decide when winning now is worth the worse position on the next trick. Leads change play order; the build does not gain permission to reorder seats.

**Shop priorities and counters.** Favor conditional ace creation and ways to control lead ownership. Opponents can force this player to lead, select a suit they cannot contest, or retain the final matching ace.

**Why it is distinct.** Crown Court values strong cards broadly; Last Word values where a strong card is played in the trick sequence.

## 11. Siege — deny the trick that makes their contract

**Win plan.** Bid conservatively enough to make the partnership's own contract, then spend resources taking the particular tricks needed to set the opponents. A set can create a larger score swing than adding a few overtricks.

**Engine and proposed sigils.**

- **Breach:** when played, reduce the rank of one opponent's card already in this trick by five; resolve the trick using the modified ranks.
- **Reconnaissance:** after bids lock, each opponent reveals one remaining spade of their choice, if they have one.
- **Trump Muster:** this card becomes a spade, providing a lead that can draw opposing trump once leading spades is legal.

Information and disruption serve a specific denial plan. Breach cannot erase the suit advantage of trump through a rank reduction alone.

**Play and partner role.** Count what the opponents still need, identify their likely winners, and attack the vulnerable suit or trump reserve. The partner cashes the partnership's reliable tricks while helping choose where denial matters most.

**Shop priorities and counters.** Prefer disruption that can change a decisive trick over bonuses for winning arbitrary tricks. Opponents can underbid, diversify their winners, or hide strength in a partner's hand. Excessive aggression can set both partnerships.

**Why it is distinct.** Its success metric is an opposing contract failure, even when that requires accepting bags or a smaller personal bid.

## 12. Bag Trap — make their extra wins expensive

**Win plan.** Make the partnership's own contract, then feed the opponents enough unwanted tricks to cross a ten-bag threshold. This is strongest when their accumulated bag count is already high.

**Engine and proposed sigils.**

- **Poisoned Gift:** after bids lock, exchange this card for a card selected by an opponent; the selected opponent receives this card.
- **Yield:** when played, decrease this card's rank by ten.
- **Empty Throne:** while held, after your partnership makes its bid, reduce the ranks of your other non-spades.

Poisoned Gift is useful when the engraved card is an awkward winner for the recipient. It exchanges cards rather than increasing an opponent's hand size or directly manufacturing bags.

**Play and partner role.** Track the opponent's bag total, retain enough tricks to fulfill your own bid, and lead suits that make their remaining winners difficult to discard. The partner must also be able to stop taking tricks.

**Shop priorities and counters.** Buy control, not unconditional weakness. Opponents can bid to absorb expected winners, shed gifts, or force this partnership to take the extra tricks instead. Near the end of a run, feeding overtricks that cannot cause a penalty may simply help them win.

**Why it is distinct.** Siege wants opponents below their bid; Bag Trap wants them sufficiently above it. The two plans can conflict within a round.

## 13. Graceful Defeat — get paid for the right losses

**Win plan.** Make a modest contract and earn extra points from selected losing cards. The player deliberately separates cards needed to fulfill the bid from cards whose job is to lose profitably.

**Engine and proposed sigils.**

- **Consolation:** when this card loses a trick, award a small round-end point bonus to its owner's partnership.
- **Honorable Loss:** if this card follows suit and loses to an opponent, award a small round-end point bonus.
- **Low Company:** while held, reduce the rank of your other cards of this suit, making their losses easier to arrange.

Honorable Loss requires an opponent to win; Consolation may also pay when the partner wins. That distinction creates different incentives and should appear explicitly on the sigil.

**Play and partner role.** Keep enough genuine winners for the bid, then place reward cards beneath higher cards. A strong partner can cover ordinary contract needs, but throwing away a required trick is rarely worth a small bonus.

**Shop priorities and counters.** Pair losing payoffs with reliable ways to lose, not with indiscriminate weakness across the entire hand. Opponents can duck, force the reward card to win, or deny the partnership's contract tricks.

**Why it is distinct.** It can operate while following suit and without a void. Unlike Ghost Hand, it expects to win some tricks and does not depend on declaring nil.

## 14. Slough Engine — profit from being unable to follow

**Win plan.** Create a void and repeatedly discard non-trump cards into other suits, earning bonus points while removing liabilities. The remaining cards fulfill a modest contract or support a partner's larger bid.

**Engine and proposed sigils.**

- **Salvage:** when this card is legally sloughed, award a small round-end point bonus.
- **Open Channel:** reveal at the start of play; the first three times you legally slough this round, award a small round-end point bonus.
- **Suit Consolidation:** before bidding, reveal this card; one other random card of its suit becomes a heart.

For these proposed effects, a slough means playing a non-trump card off suit because you cannot follow the led suit; a ruff is a separate trigger. Suit Consolidation helps only if the resulting distribution actually creates or approaches a void.

**Play and partner role.** Identify which void can produce repeated opportunities, preserve discard targets, and avoid consuming the entire hand's scoring capacity just to earn a bonus. A partner can lead into the void when the overall trick outcome is favorable.

**Shop priorities and counters.** Buy both access to sloughs and payoffs. Opponents can lead suits still held, force the player to spend cards intended for discarding, or draw trump to attack the remaining contract plan.

**Why it is distinct.** Needle spends trump to win from a void; Slough Engine spends non-trump cards to score while giving up the trick. Graceful Defeat can score losses without satisfying the off-suit condition.

## Combining archetypes

Collections should support hybrids, especially because a player buys from only three offers and engraving changes every round.

| Combination | What the combination accomplishes | Tension to preserve |
| --- | --- | --- |
| Ghost Hand + Bodyguard across partners | A protected nil plus an achievable ordinary contract | Coverage cannot guarantee every nil |
| Crown Court + Last Word | Strong cards with a plan for tied aces | Some aces must still be led or played too early |
| Relay + Needle | Exchanges finish a void and move useful trump | The partner must receive a useful hand too |
| Heart Chorus + Slough Engine | Heart concentration creates voids and supplies rewarded discards | Heart cards cannot all be spent following hearts and sloughed elsewhere |
| Diamond Investor into Crown Court | Early income purchases later contract strength | Economic sigils still occupy slots and engravings |
| Exact Contract + Bag Trap | Stop taking tricks after the bid and steer surplus to opponents | Giving away tricks too early risks a set |
| Graceful Defeat + Ghost Hand | Losing cards earn bonuses during a successful nil | Additional nil scoring needs especially careful limits |
| Spade Flood + Siege | Trump exhaustion removes the opponents' expected winners | Denial can generate costly bags |

“Into” means later purchases change the collection's emphasis; it does not assume that owned sigils can be sold or replaced. Replacement at the cap has not been established. Similarly, an archetype is a strategic plan for the current hand, not an obligation to bid the same way every round.

Adjacent-card rank bonuses can serve as a supporting package for Crown Court or Exact Contract, but should not become a separate archetype merely because they use a different targeting pattern. Their hand-ordering rules need definition before concrete sigils are finalized.

## Proposed effect conventions

These are recommendations for making the example engines coherent, not additional confirmed base rules.

- Resolve ordinary score and sigil point bonuses together at the end of a round, then calculate each player's ordinary gold award from the resulting partnership score. Add explicitly personal gold bonuses separately.
- Evaluate victory after complete round scoring so neither partnership wins merely because its score was processed first. If both reach 500, compare their scores; a tied terminal score still needs a chosen tie rule.
- Specify each sigil's timing, controller, recipients, targeting information, and lifetime. “Reveal before bidding” and “reveal after bids lock” are strategically different effects.
- Keep affinity as a placement preference, not a promise that a suitable card exists. An archetype must tolerate rounds when affinity cannot be satisfied.
- When a card moves, recommend that its engraving moves with it for the current round, while permanent ownership of the purchased sigil stays with its original owner for future deals. Sigil text must specify whether any already-revealed ongoing effect remains with its original controller.
- Resolve triggered effects once per stated event. Exchanges do not recursively trigger further exchanges unless a specifically bounded effect says so.
- A conversion or exchange occurring between tricks changes subsequent legal plays. Effects acting on cards already in a trick need explicit resolution text and cannot retroactively make a previously legal play a revoke.
- Put per-round limits on repeated score and income engines, and define how repeated copies interact. Cap the engine's total reward where necessary; limiting each copy separately may still permit excessive stacking across different cards.
- Preserve meaningful opponents' choices: targeting a visible played card is different from selecting an unknown card in someone else's hand, and an opponent-selected exchange is different from unrestricted theft.

## Remaining decisions and validation

The interview established enough to propose the archetypes, but not a full executable ruleset. The following decisions should be made before implementation or numerical balancing:

- **Rank floor:** ace is the confirmed ceiling; the minimum modified rank is unspecified. Recommend two as the floor, with low-rank ties still won by the later eligible card.
- **Shop economy:** starting gold, prices, rarity, duplicate availability, and replacement or sale rules remain unspecified. The first purchase must be affordable, and extra income must change meaningful purchase options for Diamond Investor to function.
- **Terminal ties:** define equal partnership scores when both reach 500 or round 13 ends. A shared result preserves the strict 13-round limit; a tiebreak round would extend it.
- **Hidden information and timing:** finalize reveal windows, information available in exchanges, controller changes after passing, and ordering when several effects trigger together.
- **Hand adjacency:** define whether order is fixed, canonical, or player-controlled before adding adjacency sigils; free reordering could turn a narrow positional bonus into a universal one.

Playtesting should answer the following questions rather than merely check whether each sample sigil triggers correctly:

1. Can each archetype win through its stated route against sigil-equipped opponents, and can opponents identify a practical counter?
2. Does a starter purchase offer a useful direction without requiring the player to immediately find several specific follow-up offers?
3. Does each engine survive unfavorable engraving and an ordinary bad deal, with a credible fallback bid?
4. Are Crown Court, Spade Flood, and Needle actually making different play decisions rather than buying interchangeable strength?
5. Are Heart Chorus, Graceful Defeat, and Slough Engine earning their bonuses under meaningfully different conditions?
6. Can nil plus bonus scoring reach 500 too quickly, especially since every point bonus also improves both partners' purchasing power?
7. Does Diamond Investor repay its opportunity cost before an opponent can reach 500, given the one-purchase-per-shop limit?
8. Are Bodyguard and Relay useful with ordinary partner collections, rather than requiring a perfectly coordinated paired build?
9. Does the later-card tie rule create positional decisions without making early-played aces routinely worthless?
10. Do bag and denial strategies remain situational choices, rather than turning every round into intentional underbidding or indiscriminate losing?

The design succeeds when players can explain what their collection is trying to accomplish, adapt that plan to the actual hand, and recognize when the partnership should change course.
