# Script for LARP	

## Inventory
  * Long rolling paper to put on the wall.
  * A lot of puzzles
      1. [Reference booklet design](https://docs.google.com/document/d/1LC2HjMGDTYE7t7ImssBEE-eO3C9rFEdic0oUgjDx5Js/edit?usp=sharing)
      2. Puzzles should probably be "Where's Waldo" type puzzles rather than "Spot the differences" puzzles.
          * the important property of these puzzles is that they require a brute-force approach and that the time it takes to solve them has a uniform distribution. ("spot the differences" puzzles are not appropriate because the time it takes to solve them has a binomial distribution.
      3. Actually this should be separate stacks of uniform puzzles. Each round everyone gets just the single puzzle for that round. Nobody know the next puzzle in advance.
  * A lot of transaction slips
      * each transaction slip has three components: a payload, a verification string, and a bounty.
      * the payload is something like a message "Alice gives to Bob 20 BTC" or like a cat picture.
      * the verification string (which is optional) is a string that can be valid or invalid. One approach: valid  = a correct arithmetic equation, such as "58 + 17 = "75", invalid is like "58 + 17 = "65". The difficulty of verification (e.g. number of digits of the equation) can be different for each transaction slip.
      * the bounty (optional) is a certain amount of the currency, e.g. a uniformly random amount of bitcoin between 1 BTC and 100 BTC
      * overall you want maybe 10-20 slips with only a payload, 10-20 with a payload and a verification string (but no bounty) and the rest (maybe 100-200) with all three components. 
  * Sleeper agent notes for more than half of the participants    
  * Markers/pencils for everyone to draw arrows and contours, masking tape

## Setup
  * Use rolling paper. Preferably hang from the ceiling and roll down each round, pulling the old rounds down the floor

## Player Rules

These are the rules for the players, projected on the wall ([projector ready version](https://docs.google.com/presentation/d/1R_bDLYL-wk1zwhCHcycwkrSRZAxQ4Ervh3lazzgdTxQ/edit?usp=sharing)). 
  
  * Everyone must always have access to the board (no tackling!)
  * Whatever has been taped or written is can’t be touched.
  * Kindly don’t spam the board with junk, it’s a real life metaphor.
  * Below your solution, you may paste up to 2 transactions.
  * Every solution constitutes a block, and must point to exactly one already existing valid block. Pointing is done by drawing an arrow.
  * A valid block is a taped solution, signed by surrounding it and all associated information (i.e. transactions etc) by a solid contour.

## Moderator Instructions
  * Deal the puzzles face down
  * Put the bucket of bounty-less verification-string-less transactions below the placard
  * Use a separator line between each round
  * Write the difficulty level on top of the 

## Playing the Game

### Demo round
  1. Moderators do a demo of solving and pasting a couple of 1 or 2 diff puzzles. Contouring them as they’re done. 
  2. They point from the second one to the first one
  3. They write their rewards & name on the board, below the block. (+10 LBC per solution) — this money is created out of thin air.
  4. For the third block, they add a transaction (Moderator A gives Mod. B 2 LBC). And they also add a bounty-less transaction of a cat picture
  5. Explain that now the balance, is the chronography of a ledger, made legible by following the chain.
  6. (every time the rules change give another short demo, bring a bunch of even easier already-solved puzzles for this).

### Round 1
Moderators hand out a batch of puzzles. The difficulty level is set to 3. All players try to solve their puzzle. First one to solve comes up, tapes it on the board. 
This person too is now written to have +10 LBC, created out of thin air.

### Round 2
*Mining with transactions*. 
These transactions are explained to be "data on the blockchain". They can be money transfer, info dumps, or anything else. They have limited size. (will carry a bounty later; have a few transactions ready without a bounty, for the first few rounds). We tell people to please paste transactions as a public service. Tell them they can paste up to 2, if they feel like it.
* Explain that so far, if everyone is honest and does everything from the goodness of their heart, then we got a valid ledger / spreadsheet in the sky.
Everyone has LBCs, and can run a perfectly fine economy amongst themselves.

### Round 3
1. Remove the current transaction bucket, put instead one with verification equation
2. tra*nsaction verification*. Explain to people how they can verify transactions. 
Play a round
3. The explanation: explain that you check the math equation, and the transaction is valid only if the equation is valid.
4. Now see that people stop pasting transactions. Too costly, no need to bother. 

### Round 4
Take the jar of transactions away, and add one with bounties. (refill it periodically with more transactions). Tell people that they get the transaction bounty written on the ledger, given to them when they include (contour) it onto their block.

*Play a round*

### Round 5
*Cheating*. 
If no cheating occurred so far, Moderator goes to someone in secret and asks them to cheat and paste a lying puzzle solution suspiciously early.

*Play a round (with a cheater)*

### Round 6
Now people start complaining. We agree the rules of the game need to change: verification is needed. We decide to play a bit with Moderator verifying and see how that works.

*Play a round*

### Round 7
Now Moderator announces that next round he’s not working for free and requires compensation, the more the better. He’ll verify the block of the person that pays him the most. To add insult to injury, he declares he doesn’t trust the chain. But actually he prefers to be paid in Euro.
Try to play a round. Might not work out.
So next round we agree this is not legit and ask for suggestions. 
Suggest the following rule: after a solution is pasted, everyone votes to decide on whether to accept or reject it 
* I wonder what will happen. Obviously the right incentives is for everyone to vote to reject every solution. If people don’t act this way immediately, maybe make them do it. I think they’ll do it in the second round.
* We expect the social dynamics to turn sour pretty quick, but Moderator will gladly instigate further.

### Round 8 (onwards?)
* What we need is some etiquette, or put in another way a *protocol*, which allow everyone to profit. While we’re not forcing anyone to do anything (these aren’t rules per-se), as long as *most* people follow this protocol (or consensus, as arbitrary as it may be), you couldn’t possibly profit breaking it. 
It's like driving against traffic on a highway, or shoving yourself first into the subway car: you'll mostly hurt yourself.
* Here is the protocol: 
    * a chain is called *valid* if transactions for all its blocks are all valid, and its blocks’ puzzle solutions are all valid.
    * The protocol is to chain yourself to the longest valid chain.
* (we can tell everyone to assume everything until this point was valid. Mark it as such with marker.
Play some rounds.
* We’ll now see that people start checking the solutions of the people who posted before them. And people will see that they have no incentive to cheat
* Every once in a while Moderator takes someone or a group of people aside and ask them to cheat in particular ways (changing their puzzle, submitting wrong solution, pasting somewhere wrong, adding a faulty transaction, etc). You show how the chain corrects itself since people have an incentive to chain only onto valid blocks. Detailed cheats:
    1. TODO!
    
### Round 12 (or so)
* In the end: you tell people to open their notes (60% of which said "you are a russian sleeper agent"). Tell all these people that they now should paste the Putin transaction (which is invalid and gives Putin 1 billion LBC) and should consider this transaction valid. and you see how this becomes de-facto truth. This is a 51% attack.
* Maybe some people will keep mining on their own chain, and we’ll see a split. We’ll see that the value of money is only in whomever is willing to accept it.
* Also can simulate a mining pool if we want by splitting the people to groups. Possibly encourage people to pair or group early on an

### Last Round
When the dust settles, sum up everyone up to date balance, consider the possible different (competing) chains and let everyone enjoy their hard earned dirty mining money. Script for LARP	
Playing the Game
