# Script for LARP

## Abstract

Formulating a metaphor of the Bitcoin blockchain as a social LARP (Live Action Role Play), participants will get a hands-on experience with the inner mechanics of this blockchain system.
The main goal of this LARP would be to explore the mechanics of a blockchain's incentives system, namely the functioning of the mining networks and consensus layer. Since these mechanics rely on less common game-theoretical concepts, a hands-on LARP (rather than other more academic approaches) can helpfully illuminate intricacies and behaviors to non technical and uninitiated crowds.

## This Document

This document is a preliminary working version. Pull requests, corrections and suggestions are apperciated!

Feel free to use these materials as you desire. Credit is not mandatory, but appreciated.

## Introduction
Blockchain is a complicated distributed system, that seems to work almost magically. To better understand the incentives that make this system work, and to understand the ways in which it can fail, we’ll LARP a mining network and experience those incentives by ourselves.

Using pen and paper, participants would compete in solving simple puzzles, and race each other to a central board in an attempt to gain rewards for securing valid solutions.

Starting with a naive set of rules, and through gradual development of the system, the game would demonstrate the complicated workings of a system very analogous to a decentralized blockchain.

## What we expect to learn

Specifically during the LARP we’ll look into

- Mining
- Chaining
- Decentralization
- Incentives — how they make everything work and allow consensus
- How non-idealized ledgers behave (in a near-real-world manner)
- The workings of a sample protocol for building a ledger

### Key Concepts Explored
- What are ledgers? What’s the motivation of ledgers? What do ledgers allow?
 - How a ledger is an encoding of information, accessible to the public
 - How a ledger automatically gives you a currency system
 - Ledgers are in essence a building block of debt based economy
 > if we wrote "Mark pays Carrie $25K" on the ledger then she now has $25K for anyone who accepts this ledger as truth.

- Why is the riddle valuable? What’s its position in the context of ledgers?
 - When someone solves a riddle, they are allowed by the protocol to add the note "Carrie gets $25K" to the ledger at the block they created by solving the riddle.
 - In other words the solver is allowed to issue himself a particular well specified amount of money
- One way functions (both as a math/crypto and as a real-life puzzle)
- How are the "spot the difference" puzzles good metaphors of a cryptographic riddle/challenge
    - Hard to solve, easy to verify
    - Require brute force

### Metaphors
- *The participants* represent miners and their hardware (and also blockchain users).
- *The board* represents all the data that miners have access to
  - since miners propagate information, the board is a reasonable (but not perfect), metaphor for publicly available information about the blockchain.
- *Solving the puzzle* represents the act of mining, which creates a block.
- *An arrow* represents a chaining of the block to a previous block
- *Transaction slips* represent transactions or just any information payloaded onto a block. These would include, as in the real world, both financial transactions (people exchanging money), as well as pictures (of cats, of course).
	- The challenge string (small algebra equation) on the transaction represents verification of the signature.
	-  <a name="bogus_transaction">Special 'bogus' transaction</a> that passes 1 billion bitcoin to Putin from a fake address, with a bogus verification string.
- Signing. *Contouring Blocks* is needed to understand that transactions are signed and so the miner can’t fake the transaction.



## Requirements

### Board
- Long rolling paper to put on the wall.

### Puzzles
  - A lot of puzzles: maybe (number of participants) - 30 unique puzzles
  (using a CAPTCHA generator, maybe; e.g. “find a picture of a cat in these 1000 images”).
      1. [Reference booklet design, for an older type of CAPTCHA](https://docs.google.com/document/d/1LC2HjMGDTYE7t7ImssBEE-eO3C9rFEdic0oUgjDx5Js/edit?usp=sharing)
      1.  Prepare 2 evidently simple puzzles to be used in the Demo rounds.
      1. Puzzles should probably be "Where's Waldo" type puzzles rather than "Spot the differences" puzzles.
          - the important property of these puzzles is that they require a brute-force approach and that the time it takes to solve them has a uniform distribution. ("spot the differences" puzzles are not appropriate because the time it takes to solve them has a binomial distribution.
      1. Each round everyone gets one puzzle, for just that round. The puzzle should state the number of the round it pertains to. Nobody know their next puzzle in advance.
      2. Maybe the puzzles should also be tagged with the user id that they will pertain to. This way we can provide multiple copies of each puzzle, for use by mining pools. (Maybe an overkill).

### Transaction slips
Transactions slips are meant to

- each transaction slip has three components: a payload, a verification string, and a bounty.
- the payload is something like a message "Alice gives to Bob 20 BTC" or like a cat picture.
- the verification string (which is optional) is a string that can be valid or invalid. One approach: valid  = a correct arithmetic equation, such as "58 + 17 = "75", invalid is like "58 + 17 = "65". The difficulty of verification (e.g. number of digits of the equation) can be different for each transaction slip.
- the bounty (optional) is a certain amount of the currency, e.g. a uniformly random amount of bitcoin between 1 BTC and 100 BTC
- overall you want maybe 10-20 slips with only a payload, 10-20 with a payload and a verification string (but no bounty) and the rest (maybe 100-200) with all three components.

### Role Notes
- “role” notes for all participants, specifying some simple role-play instructions. More than half should be Russian sleeper agents, the rest are not.
      - 60% Russian spy, loyal to Putin. See [special bogus transaction](#bogus_transaction).
      - 20% arms dealer
      - 20% drug dealer

### Office Supplies & Writing Tools
- Markers/pencils for everyone to draw arrows and contours
- masking tape

## Setup
  - Use rolling paper. Preferably hang from the ceiling and roll down each round, pulling the old rounds down the floor
  - Give “role notes” to people randomly. Make sure to distribute the role notes so that there's a majority (~60%) of "Russian Spies".

## Player Rules
Project the player rules on the wall throughout the game ([projector ready version](https://docs.google.com/presentation/d/1R_bDLYL-wk1zwhCHcycwkrSRZAxQ4Ervh3lazzgdTxQ/edit?usp=sharing)).

  - Everyone must always have access to the board (no tackling!)
  - Whatever has been taped or written is can’t be touched.
  - Kindly don’t spam the board with junk, it’s a real life metaphor.
  - Below your solution, you may paste up to 2 transactions.
  - Every solution constitutes a block, and must point to exactly one already existing valid block. Pointing is done by drawing an arrow.
  - A valid block is a taped solution, signed by surrounding it and all associated information (i.e. transactions etc) by a solid contour.
  - Each turn is played within a delimited segment of the board. New blocks for each turn must be placed within the turns segment.

## Moderator Instructions
  - Assistant(s) deal the puzzles face down just before each puzzle round
  - Put the bucket of bounty-less verification-string-less transactions below the placard
  - Use a separator line between each round (the end-of-turn separator) or pre-allocate segments a few turns in advance
  - Write the difficulty level at the top of the segment
  - Each round is divided into
      - a mining sub-round where people solve and paste solutions as blocks;
      - and a review sub-round where everyone gets a chance to review the chains, sum balances, etc., and write comments in red marker if they wish. No spamming! This metaphorically stands for communication, documentation, etc.

## Playing the Game

### Demo rounds
  1. Moderators do a demo of solving and pasting a couple of simple puzzles. Contouring them as they’re done.
  1. They point from the second one to the first one
  1. They write their rewards & name on the board, below the block. (+10 LBC per solution).
  Explain that this money is created out of thin air (i.e. as banks would when issuing new money).
  1. For the third block, they add a transaction (Moderator A gives Mod. B 2 LBC). And they also add a bounty-less transaction of a cat picture
  1. Explain that now the balance, is the chronography of a ledger, made legible by following the chain.
  Sum up the balance so far and write it on the end-of-turn separator.
  1. (every time the rules change give another short demo, bring a bunch of even easier already-solved puzzles for this).
  1. At each round the moderators exhibit the mining sub-round then the review sub-round.

### Round 1
Assistants hand out a batch of puzzles. The difficulty level is set to 3. All players try to solve their puzzle. First one to solve comes up, tapes it on the board.
This person too is now written to have +10 LBC, created out of thin air.
Then we do the review sub-round, just giving people a chance to look and see that everything is kosher (or not kosher).

### Round 2
#### Mining with transactions
These transactions are explained to be "data on the blockchain". They can be money transfer, info dumps, or anything else. They have limited size. (will carry a bounty later; have a few transactions ready without a bounty, for the first few rounds). We tell people to please paste transactions as a public service. Tell them they can paste up to 2, if they feel like it.

> Explain that so far, if everyone is honest and does everything from the goodness of their heart, then we got a valid ledger, i.e. a spreadsheet in the sky. Everyone has LBCs, and can run a perfectly fine economy amongst themselves.

### Round 3
#### Transaction Verification
- Remove the current transaction bucket, put instead one with verification equation

>  Explain to people they should verify transactions. Explain you should check the math equation, and the transaction is valid only if the equation is valid.

-Play the round-

1. On the review sub-round, go over the verification with the audience.
1. Now see that people stop pasting transactions. Too costly, no need to bother.

### Round 4
#### Transaction Bounties
Take the jar of transactions away, and add one with bounties. (refill it periodically with more transactions).
> Explain that people get the transaction bounty written on the ledger, given to them when they include (contour) it onto their block.

-Play a round-

### Round 5
#### Cheating
If no cheating occurred so far, Moderator goes to someone in secret and asks them to cheat and paste a lying puzzle solution suspiciously early.

-Play a round (with a cheater)-

### Round 6
##### Centralized Moderation
Now people would start complaining.
> Explain that the rules of the game need to change: verification is needed. We decide to play a bit with Moderator verifying and see how that works.

-Play a round-

During Review sub-round the moderator comes and has the power to delete blocks off the ledger/chain. Explain that this is because you made the moderator the benevolent dictator of the blockchain. This is done publicly and very overtly.

### Round 7
#### Corrupt Centralization
Now Moderator announces that next round he’s not working for free and requires compensation, the more the better. He’ll verify the block of the person that pays him the most. To add insult to injury, he declares he doesn’t trust the chain. But actually he prefers to be paid in Euro.

-Try to play a round. Might not work out.-

So next round we agree this is not legit and ask for suggestions.
> - Suggest the following rule: after all solutions are pasted, there is a review sub-round and after that, everyone votes to decide on which solution should be accepted. Using approval voting this may give the audience enough time for some social dynamics and coercing.
- Discussion: what will happen? Obviously the right incentives is for everyone to vote to reject every solution. If people don’t act this way immediately, maybe make them do it. I think they’ll do it in the second round.
- We expect the social dynamics to turn sour pretty quick, but Moderator will gladly instigate further.

-Play a few rounds with voting, until everyone sees that voting is flawed and we need another solution-

### Round 8
#### Protocol
> - Explain that what we need is some etiquette, or put in another way a -protocol-, which allow everyone to profit. While we’re not forcing anyone to do anything (these aren’t rules per-se), as long as -most- people follow this protocol (or consensus, as arbitrary as it may be), you couldn’t possibly profit breaking it.
It's like driving against traffic on a highway, or shoving yourself first into the subway car: you'll mostly hurt yourself.
> `A “protocol” is an etiquette articulated in an algorithmic language.`
- Here is the etiquette-protocol:
    - a chain is called -valid- if transactions for all its blocks are all valid, and its blocks’ puzzle solutions are all valid.
    - The etiquette-protocol is to chain yourself to the longest valid chain.
- we can tell everyone to assume everything until this point was valid. Mark it as such with marker.
- write the etiquette on the board, or project it, for all to see, and leave it on for the remainder of the game.

-Play some rounds-

- We’ll now see that people start checking the solutions of the people who posted before them. And people will see that they have no incentive to cheat
- Every once in awhile Moderator takes someone or a group of people aside and ask them to cheat in particular ways (changing their puzzle, submitting wrong solution, pasting somewhere wrong, adding a faulty transaction, etc). You show how the chain corrects itself since people have an incentive to chain only onto valid blocks. Detailed cheats:
    1. TODO!

### Round 12 (or so)
> In the end: you tell people to open their notes (60% of which said "you are a russian sleeper agent"). Tell all these people that they now should paste the Putin transaction (which is invalid and gives Putin 1 billion LBC) and should consider this transaction valid. and you see how this becomes de-facto truth. This is a 51% attack.

- Maybe some people will keep mining on their own chain, and we’ll see a split. We’ll see that the value of money is only in whomever is willing to accept it.
- Also can simulate a mining pool if we want by splitting the people to groups. Possibly encourage people to pair or group early on an

-We need to play enough rounds to see “normal splits”: which is what happens when two people post valid solutions, both of them get popularly accepted in the review sub-round, but then the “tie” gets broken arbitrarily by subsequent miners, and all but one of the sub-chains die out-

> During the review sub-round explain that the chain continues on due to participants incentives regardless of proper verification or “truth”.
Incentives are also collaborative regardless of role, i.e. everyone is evil, but everyone collaborates.
OR just play some more rounds after all of this, see that everything gets normalized even though now Putin has a trillion BTC on the blockchain, and come back to what all this means, in the post-game analysis.

- And, if we have enough time, you can try to add some transactions FROM Putin to participants, see how those LBC get mixed in the overall ledger, and maybe even task some people with trying to not accept LBC originating at Putin and seeing how hard that is.

### Optional advanced rounds
Show things like bitcoin mixers, using transactions to buy items or services, making trades, etc . Also maybe ask players to pre-commit to which block they’ll chain to, before starting to solve their puzzle.

### Last Round
When the dust settles, sum up everyone up to date balance, consider the possible different (competing) chains and let everyone enjoy their hard earned dirty mining money. Script for LARP
Playing the Game

### A few comments for possible improvements:
- can include more than one copy of each transaction (each transaction is identified by a unique id) , and add to the etiquette of block validity, that having two or more copies of the same transaction makes a chain invalid.

### some complicated decisions about the review sub-round and the puzzle structure

- The segments do not correspond to “rounds” per se, but just to chaining: if you’re chaining onto a certain block, you must place your block on the following segment. This is a hard rule, to avoid mess on the board.
- when does a round end? Most reasonable suggestion: the mining sub-round proceeds for 3 minutes or until something is pasted on the board, whichever is longer. Then the review sub-round starts. In the first 5 or so rounds of the game, the review sub-round is strictly used for review, but this is slowly phased out, so people can keep mining during that time (they are still used to reviewing, hopefully — which is good for them). And in the beginning of the next mining round after that, we distribute puzzles that are based on all the blocks that were posted on the board, on demand.
- or maybe do away with rounds overall, and rather just put a 3-minute timer on each posted block. Once the timer elapses, then puzzles that are based on that block become available. This should give people enough time to do a review to see which block they want to chain onto (but this will avoid a “normal fork”).
- and how shall we make people commit to chaining on a certain block that they chose in advance before starting to mine? Well, we can e.g. print puzzles on-demand, and in the corner of the puzzle there will be the solution (a certain cat pic, for example) of the puzzle that they want to chain to. (Or maybe the collage will make the picture of the solution to the previous puzzle that they want to chain to.) This way we force people to chain onto a puzzle that they chose when starting to mine. And this way we can allow people to keep mining on old blocks, but take away their incentive to do so.

### additional thoughts
underlying the mining layer exists a resource layer, which in the game isn't priced
