_This document is a work in progress, please make PRs_

----------------------------------------
# Preamble

## Declaration of Genesis
There comes a time when there is enough disagreement among community members
and stakers about the core decisions of the hub, such as its purpose and
architecture and risk tolerance, that it makes the most sense to support
alternative opinionated forks running alongside the original hub to be prepared
against all contingencies, with the added benefit that it can operate as a
(political) party base with governance fully or partially delegated to the
party hub. (this is fine so long as every party is afforded this tool, and as
long as it isn't offered misleadingly say as a collective "liquid staking"
service).

This seems like a natural and necessary way to split the community to enable a
diverse ecosystem of specialization and coopetition and minimize friction.
Having this as the goal gives us the directivec and opportunity to develop a
robust antifragile ecosystem that doesn't suffer from systemic risk of
cascading failures. 

### Context and Need for the Fork: In recent times, the Cosmos community has
faced significant challenges and disagreements among community members about
moving forward. These challenges have underscored the need for an alternative
approach, leading to the creation of this fork. Our aim is to address these
issues head-on, providing a platform for resolution and progress.

### Vision and Goals: The vision behind this fork is to an alternative fork
running on standby to prepare for all contingencies, and also operating as
political party base. We strive to complement the broader Cosmos ecosystem,
while introducing innovative solutions and perspectives. Our goals are not just
to resolve current challenges but to set a precedent for adaptive and
responsive governance in decentralized networks.

### Role of the Fork in the Ecosystem: As a new branch within the Cosmos
ecosystem, this fork will prepared a minimal hub. We anticipate that our
approach will not only enhance the functionality of the Cosmos network but also
enrich its diversity and resilience.

### Significance as a Political Base: Operating as a "political party base,"
this fork will serve as a hub for ideation, discussion, and decision-making. It
aims to empower community members to actively participate in governance and
influence the future trajectory of the ecosystem. This approach is expected to
bring a more democratic and transparent governance process to the Cosmos
community.

### Expected Outcomes and Benefits: We believe that by embracing diversity and
fostering open dialogue, we can achieve a more robust and innovative ecosystem.
The benefits will extend beyond immediate technical solutions, contributing to
a more vibrant and collaborative blockchain community.

## Terms

* Decentralists: github.com/decentralists is the name of the party.
* AtomOne: is the name of the hub of the party.
* Constitutional Majority: some higher bar than 2/3, say 90%.

----------------------------------------
# Objectives

These objectives all users and members should agree with, and must be reflected
in the constitution and code of the atomone software (including ICS1.5). These
objectives can only be changed througha Constitutional Majority (significant,
more than two thirds).

## 1. Define $ATOM1

The $ATOM1 is defined to be the staking token of the larger continuous minimal
ICS IBC Cosmos Hub that keeps 2/3 of $ATOM1s staked.

In the case of forks or splits, the $ATOM1 token is the one that has the larger
relative market cap, of those forks and splits where the distribution is a pure
opinionated fork of the last $ATOM1 distribution which, at that moment of
publishing to the users of the chain, had uncontended consensus.

A pure opionated fork is a fork of the original distribution where 100% of the
distribution is air-dropped to original staking token holders after applying
any slashing based on the application of a slashing strategy consistent with
the philosophy of the new fork; including and up to 100% for slashing based on
a staker's validator's actions, and the staker's own actions (or inactions).

No additional premines besides those already defined in this planning document
are allowed for any forks whose token is called $ATOM1.

## 2. Hub Minimalism

Hub minimalism does not mean that the functionality of the atomone hub is
restricted; but it does imply among other thigns that the main hub chain's
logic is reasonably restricted to those that coordinate the many shard (or
consumer) chains.

In particular, the hub's root chain lacks a complex VM implementation, but
rather requires VMs to live on other non-root shards.  This is the best way to
scale to billions of users while providing specialization and isolation. For
example, your home internet WIFI network is provided by a minimal router
hardware, while your backup harddrives and your desktop computer are separate
machines that only connect to the router.

Any fixed functionality that could run on alternative VMs should be translated
into the dominant language of the official approved software, which for us is a
recent version of Go(lang) 1.xx. We should remind ourselves that every virtual
machine has (had) numerous zero day exploits. The added security vulnerability
surface area of the new VM combined with the compiler to compile one languge
for the VM, as well as the added complexity of needing to audit another
language, can and must all be avoided.

Mixing implementations across validators is also to be avoided so as to prevent
a failure arising from a low Nakamoto coefficient among the types of
implementations.

Arbitrary smart contract functionality should not be allowed on the main hub
chain, which should instead be reserved primarily for ICS1.5 shard coordination
and governance voting as safety and liveness critical functionality.

## 3. Validator Incentives

Fix Validator incentives so that every validator is PAID to run ICS consumer
chains and hub shards. Actually model the minimal economic model that describes
physical reality sufficiently to be intuitive and adaptive to all scenarios.
Every ICS pays supermajority to validators!

## 4. Governance

See [github.com/decentralists/DAO](https://github.com/decentralists/DAO/tree/main/governance)

Fix governance. We already have proposals in the works on github decentralists
DAO / governance. Contribute there so that Governance is fixed and we stop
spending money like a flock of headless geese.

## 5. "Liquid Staking"

Fix "liquid staking". What we have isn't liquid staking, they are "partyhubs".
What people want are liquid fungible tokens that aren't so inflationary, I get
it. ICS scaling will fix the problem, but if you really want more, fix LS to
delegate pro-rata, NOT have its own gov. Or, over time, possibly create a
bicameral gov structure w/ exponentially inflating $ATOM1 stakers, and limit
how $PHOTON reverts to $ATOM1 to prevent hostile takeover.  VP(staked $ATOM1)
>= VP(all $PHOTON).

TODO: Comparison between liquid staking and (collective) "liquid staking".

Later we show the $phATOM token which is deflationary AND liquid, yet fully
backed by $ATOM1s.

## 6. Declaration of Independence & Constitution

Adopt a Declaration of Independence and Constitution with cryptographic
signatures.

See [draft declaration](./TODO) and [draft constitution](./CONSTITUTION.md).

## 7. IBC1.5

Solve IBC1.5, or ICS1.5, where the validator sets are implicit, for fast
inter-hub communication with implied IBC, WITHOUT sacrificing independent BFT
consensus layers.

XXX add more

## 8. Transparent Security System

Create a permissioned and completely accountable and 100%
predetermined-finite-time-delayed transparent security reporting system where
ABSOLUTELY EVERYTHING within it eventually becomes public knowledge to help
deal with zero day vulnerabilities and current attacks & fund it.

## 9. Fund SubDAOs

Create and support competing marketing, growth, infra, dapp subDAOs, and
especially help them foster the best in class in Cosmos; from the user level
down to the VM, every component should have a good selection of competition.

See https://gitub.com/gnolang/gno
TODO add more smart contract projects.

## 10. Engineering Task Force

Create a team tasked with minimizing and simplifying code and reducing
unnecessary dependencies, taking the best examples from various forks taken
into consideration, so that all the best ideas from all forks can integrate
into one where-ever possible. FINISH software.

See https://github.com/gnolang/gno/tree/master/tm2 for Tendermint2

## 11. Enable Meiosis

Ossify the partyhub after it has become its own competing IBC/ICS hub.  Allow
others to likewise fork from you by enabling ICA partyhubs when there is
disagreement. Multiply by meiosis and conquer the world.

See https://github.com/gnolang/gno/pull/1224 for prototype WIP of splitting.

----------------------------------------
# Plan

The AtomOne hub exists as a separate minimalist fork of Gaia. Both are separate
and distinct from gno.land, though gno.land and the GnoVM (as well as other
VMs) will play significant roles in completing the hub and maintaining its
upkeep.

The main goal is to fix what must be fixed in governance and the need for an
explicit constitution, before launching the full IBC and ICS functionality of
the chain.

First we describe the tokenomics of the atomone hub, followed by the main
milestones, with an emphasis on completion and even phase-out.

## Genesis Distribution

It should be some distribution of the Cosmos Hub $ATOM1 token with those who
voted against the spirit of this project slashed because they never joined to
use the system int he first place (e.g. they were more interested in price
appreciation of original $ATOM).

Additionally, the Interchain Foundation playing a key role in the evolution of
the hub, should also be removed.

Finally, 10% of the $ATOM1s are premined for various purposes.

The $ATOM1s in genesis are locked and cannot be transferred due to the value of
the parameter ENABLE_SENDTX except for chosen addresses (e.g. for faucets).

The Genesis Distribution is largely an opinionated fork of the cosmoshub4 $ATOM
(judged by alignment based on voting activity, to slash those who don't align,
or those who aren't interested in using our chain).

The Interchain Foundation will be excluded from this distribution, so as to create
a separation of concerns, and instead 10% of the final total amount will be
allocated toward contributors and onchain DAOs.

Of the 10% premine, 
 - 1% to general pre-launch contributors and early adopters.
 - 1% reserved for IBC contributions (and all that it entails) and early
   adopters.
 - 1% reserved for ICS1.5 contributors (and all that it entails thereafter)
   and early adopters.
 - 7% reserved for gov distribution to subDAOs for remainder of plan and
   constitution (but nothing more).

In addition to these premines, the earned tax revenue (rewards) and inflation
will be split as per the following:
 - 80% of the inflation+rewards going to the stakers who select validators.
 - 10% of the inflation+rewards going to active validators equally.
 -  5% of the inflation+rewards going to general commons pool with no standalone governance.
 -  2% of the inflation+rewards going to pool for open source blockchain explorer hosting.
 -  2% of the inflation+rewards going to pool for securing open source wallet systems (w/ airgap).
 -  1% of the inflation+rewards going to pool for public relations and growth.

A parameter MIN_STAKER_DISTRIBUTION_FRACTION will be set to 80%, where the
percent of inflation+rewards going to stakers cannot be lower than this figure.
Changing this value requires a constitutional majority.

A parameter MIN_VALIDATORS_DISTRIBUTION_FRACTION will be set to 10%, where the percent
of inflation+rewards going to stakers cannot be lower than this figure.

The funds held in all the pools above will not be counted toward the bonding ratio.

The last three following the pool/treasury will intially go to multisigs set in
consensus params of the chain, until they get set as URIs pointing at
blockchain based DAOs hosted on ICS1.5.

## Tokenomics

We opt to replace the market-based "commission" system with a flat
distribution to all validators, to incentivize the creation of peer validators
(who should all plan to become datacenter providers). 

The maximum bounds on the auto-adjust inflation parameter will be set at 20%.

The inflation will target 2/3 of $ATOM1 to be bonded. 

### ICS Fee Distribution
Every ICS zone should be paid for somehow. AtomOne owned ICS shards should be
paid for from the treasury of AtomOne.  Other ICS "consumer chains" can be paid
for by the the chain itself, and in emegencies anyone can step in and pay on
the zone's behalf. 

In short, every ICS zone should be profitable to every validator.

The DISTRIBUTION_FRACTION parameter is the fraction (between 0 and 1) of ICS
shard and consumer chain payments that are shared among the validators equally.
This is initially set to 0.8, giving the majority to the validators, and only
20% as royalty to be paid to $ATOM1 stakers, with the COMMUNITY_TAX taking its
portion.

### Staking

The main difference being introduced is that the total amount of stake going to
one validator doesn't actually increase the validator's power, even though all
of those staked $ATOM1s are at stake should this validator get slashed. This
creates a potential exploit opportunity whereby some validators have relatively
little at stake, and 1/3 by total of voting power of those tial validators end
up causing a double spend attack. To prevent this, overstaking to a validator
will be taxed incrementally with the proceeds going toward general rewards.

XXX TODO improve this. Maybe instead there is simply a sqrt(vp) applied to all
the voting powers after the original Gaia staking algorithm. You can over-stake
to a validator but your voting power and returns will be much less, almost
inverse to the amount of overstaking.

Suppose that 1/3 of the $ATOM1 stakers are slashed due to a complex double
spend attack. Assuming that we want to allow the recompensation of victims upon
double spend attacks (within the bounds specified clearly in the constitution)
only from the recently slashed $ATOM1s, some nonzero portion of the slashed
stake must be burned to prevent using the double spend attack as a fast way to
unbond.

If no victims need to be made whole, then it could be appropriate to burn the
slashed $ATOM1s of the perpetrators. The end result is that the remaining
stakers own the network, and in a steady state this would result in the price
of $ATOM1s increasing due to the reduced supply, assuming that the convidence
and usage of atomone hasn't changed; though in perfect theory it should take a
bit of a hit, at least in proportion to the destruction of the reputation of
those validators.

If victims are to be made whole with slashed $ATOM1s, this may require the
selling of $ATOM1s into the market, or result in it, therefore the price of
$ATOM1s will be pushed lower, and the composition of the $ATOM1 holders mutated
according to market conditions.

### $phATOM the Deflationary Derivative of $ATOM1

$ATOM1 isn't a monetary token, but a related instrument can serve better as
one.

Auto-staking (staking across all validators proportionally to existing voting
power) doesn't solve the "inflation problem", but it does give a way for people
who don't care about staking decisions to make better-than-random staking
decisions.

TODO show simplest example that demonstrates slashing.

Auto-staking if done by an external IBC zone, or an individual staker manually,
would like any other staking earn the pro-rata revenue and pay the various
taxes. So auto-staking per se does not make for a deflationary holding, but it
comes with the benefit of automatic diversification.

Since it comes with benefits to the staker (diversification and thus less risk)
but it doesn't provide the needed intelligence to atomone, it is better for the
atomone hub to provide a standard minimal correct implementation under its
control, such that it can also regulate it, especially as it relates to control
over atomone governance. 

Say when you auto-stake $ATOM1 through this sanctioned mechanism, you get
$phATOM. In order to incentivize the usage of $phATOM, the atomone hub offers a
trade that makes $phATOM deflationary: non-atom rewards nor taxes are applied
to auto-staked $ATOM1 bonded $phATOM holders, and with the right conversion
equation (which adjusts for $ATOM1 inflation) we can construct a perfectly fixed
$phATOM supply (say of 1 billion $phATOMs) no matter how many $ATOM1s bond to
$phATOMs.

Should this "more monetary" construction of the fixed supply ("deflationary")
$phATOM token incentivize a large liquid supply, it becomes more susceptible to
hostile takeovers, simply because there are more liquid $ATOM1 staking tokens
available in comparison to the total bonded voting power. Therefore for a more
secure atomone hub we also limit the conversion back from $phATOM to $ATOM1 so
as to make hostile takeovers more expensive.

The known ways are: 
 * Widen the gap in bidirectional conversion price between $phATOM and $ATOM1.
 * Limit the amount of $ATOM1 that can be released per time period auction.
 * Essentially the same as above with some conversion curve.

In the case of validator & delegator $ATOM1 slashing, $phATOM holders will of
course also get slashed, but the ratio of $phATOM-bonded $ATOM1s and all other
(non-$phATOM) $ATOM1s remains the same. The conversion factor from $phATOM to
$ATOM1 will change because of slashing, but the conversion factor from $ATOM1
to $phATOM will not before and after slashing, thereby making the total
possible supply of $phATOM lower than before (more deflationary) and over time
making the cost of conversion to $phATOM more expensive in comparison to the
inverse, thereby allowing the exchange rate between the two tokens to naturally
float between two reasonable bounds.

NOTE: This uses the market imperfection of the $ATOM1 and $phATOM tokens to
create a (larger) gap in the conversion price, thereby making the tokens more
independent of each other. $phATOM holders might be happy that their token has
become more deflationary (total supply reduction), and while they can only get
the post slash amount of $ATOM1s, the value of those $ATOM1s might be preserved
or catch up soon after new validators start operations. The alternative where
the total amount of $phATOM remains invariant in comparison appears strictly
worse for $phATOM holders. This widening of the gap could in theory happen at
any time with governance.

The $ATOM1s bonded toward auto-staking does not count toward calculating the
bonding ratio target of 2/3 in either the numerator or denominator--they are
ignored.

TODO: add benefits over liquid staking and collective "liquid staking".

## AtomOne Governance

Ultimately this hub is owned by the $ATOM1 holders. 

We will prioritize all of these items:
[github.com/decentralists/DAO](https://github.com/decentralists/DAO/tree/main/governance)

The constitutional majority threshold is defined by the parameter
CONSTITUTIONAL_MAJORITY_THRESHOLD initially set to 90%, and requires a
constitutional majority to change.

The constitution itself must be amended by a constitutional majority.

## Milestones

There are largely four phases to this plan.

### AtomOne Phase 1: Pre-IBC

1. Define Constitution
2. Governance Fixes
3. Launch Governance-Only Chain
4. Implement IBC

### AtomOne Phase 2: Post-IBC

1. $PHOTON with Auto-Staking
2. Fix Validator Incentives
3. Implement ICS1.5
4. Prototypes with SubDAOs (including GNO)

### AtomOne Phase 3: ICS1.5 scaling

1. Migrate $PHOTON to ICS
2. Promote Smart Contract Use Cases
3. Develop Scalable Validator Infrastructure
4. Develop Recovery Preocedures

### AtomOne Phase 4: Maintenance

1. Create OnChain Education Curriculum
2. Promote Good Forks and Projects
3. Promote Other Common Goods
4. Finalize the Software

Finalization should not be seen as a thing to avoid, but rather a necessity for
preserving immutability and thus providing real security benefits.

Everyone who wants something different is given a way to create their own
variation to compete and cooperate with the atomone hub. We should all be
familiar with this concept, as it is how atomone itself was born--by exodus
from Gaia.

It is possible that what we arrive at is not sufficient in the long run, and
that is still OK; the ultimate goal is to be a standard reference, in the very
least in relation to an improved fork; a reference that will last a thousand
years or more.

In short, the goal is nothing more than to create timeless code, even knowing
that in the end even atomone will be phased out, but never forgotten; the
template will have split into a million different forks and conquered the
world.

AtomOne Eschatology will be well documented and planned, for a time when nobody
was around for these early beginnings.

----------------------------------------
# FAQ

## AtomOne vs Gaia

AtomOne is just built different.

## AtomOne vs Gno.land

Gno.land will be a hub for GnoVM based smart contracts. It may benefit from
ICS1.5 in the future, but we will first offer GnoVM scaling on the AtomOne ICS
economic zone. Gno.land will not connect to Gaia except indirectly through
atomone, or its minimal successor.

## AtomOne & Tendermint2

NewTendermint, LLC will lead Tendermint2 development, and AIB, Inc will
contribute by building its own engineering team within AIB, Inc that will
transition into long term co-maintainers of atomone, and co-members of
gno.land. 

AtomOne is a collaborative project that includes many members including AIB Inc
and NewTendermint, LLC. Any rights to the brand of AtomOne that NewTendermint
might have (or not have) is donated to the sovereignty of the atomone hub, or
managed by AIB Inc on behalf of the hub.

----------------------------------------
# TODO

 - [ ] Complete the CONSTITUTION w/ all known functionality
 - [ ] Reconcile this README with CONSTITUTION
 - [ ] Incorporate the "Constitutional Majority" in the Constitution.
 - [ ] Check for consistency w/ Decentralists DAO governance roadmap.
 - [ ] XXX
