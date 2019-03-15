# Terms and Definitions

[TOC]


## __Block__

A collection of data, such as transactions, that together indicate a state transition of the blockchain.

## __Block explorer__

An application which allows a user to explore the different blocks on a blockchain.

## __Bonding__

A process by which tokens can be "frozen" in exchange for attaching a parachain to a relay chain.  This process ensures that only chains that are valid and running will be attached to the relay chain, as it would behoove DOT holders to stop bonding their tokens.

## __Bridge__

A node which acts as an intermediary between the Polkadot relay chain and an external chain, in such a way that it appears to the relay chain that the external chain is a parachain (i.e., meets the Polkadot Runtime Environment requirements).  Bridges allow for interaction between other blockchains such as Ethereum and Bitcoin which are not natively compatible with Polkadot.

## __Byzantine Fault Tolerance__

The property of a system which is tolerant of Byzantine faults; that is, a system where not only may individual subsystems fail, but it may not be clear if a particular subsystem has failed or not.  That is, different observers on the system may not agree on whether or not the system has failed.  Ensuring Byzantine fault tolerance is an important part of developing any distributed system.

## __Collator__

A node which maintains a parachain by collecting parachain transactions and producing state transition proofs for the validators.

## __Consensus__

The process of a group of entities to agree on a particular data value (such as the ordering and makeup of blocks on a blockchain).  There are a variety of algorithms used for determining consensus.  The consensus algorithm used by Polkadot is GRANDPA.

## __DOTs__

The native token for Polkadot.  DOTs serve three purposes: network governance (allowing them to vote on network upgrades and other exceptional events), general operation (rewarding good actors and punishing bad actors), and bonding (adding new parachains by "freezing" DOTs while they are connected the relay chain).

## __Dapp__

A generic term for a decentralized application, that is, one which runs as part of a distributed network as opposed to being run on a specific system or set of systems.

## __Extrinsic__

Generically, some function declared by the programmer, i.e., one that is not buil

n to the language or framework.  Specifically for Polkadot, this refers to a binary blob which represents some state transition (such as a transaction) and is used for parachains to communicate via the relay chain.

## __Finality__

The property of a block which cannot be reverted.  Generally, created blocks are not final until some point in the future

perhaps never, in the case of "probabilistic finality" such as in Bitcoin (although Bitcoin blocks are generally considered "final" after six confirmations due to the unlikelihood of reverting at that point).  In the Polkadot relay chain, the goal is for blocks to be finalized 1

2 seconds after creation.

## __Finality Gadget__

A mechanism which determines finality.

## __Fisherman__

Nodes which monitor the network for validators or collators which are behaving badly.  Fishermen must stake a small amount of DOTs but can be rewarded greatly if they find bad behavior.

## __GRANDPA consensus algorithm__

GHOST-based Recursive Ancestor Deriving Prefix Agreement.  It is the finality gadget for Polkadot, which allows asynchronous, accountable, and safe finality to the blockchain.  For an overview of GRANDPA, see this Medium post: [https://medium.com/polkadot-network/polkadot-proof-of-concept-3-a-better-consensus-algorithm-e81c380a2372](https://medium.com/polkadot-network/polkadot-proof-of-concept-3-a-better-consensus-algorithm-e81c380a2372)

## __Governance__

The process of determining what changes to the network are permissible, such as modifications to code or movement of funds.  The governance system in Polkadot is 

chain and revolves around stakeholder voting, i.e. the majority of the stake (DOTs) determines the direction of the network.

## __Governance Council__

An on-chain entity which consists of several on-chain accounts (starting at 6, eventually moving to the final value of 24) which can act as a representative for "passive" (non-voting) stakeholders.  Council members have two main tasks: proposing referenda for the overall stakeholder group to vote on and cancelling malicious referenda.

## __LIBP2P__

An open-source library for encrypted peer-to-peer communications and other networking functionality.  More information at: [https://libp2p.io/](https://libp2p.io/)

## __Liveness__

The property of a distributed system that it will eventually come to some sort of consensus.  A system stuck in an infinite loop would not be considered live, even if computations are taking place; a system which eventually provides a result, even if incorrect or it takes a long time, is considered to have liveness.

## __Node explorer__

A tool which gives you information about a node, such as the latest blocks sealed, finalized, and the current chain state as known by that node.

## __Nominated Proof of Stake (NPoS)__

A proof of stake system whereby nominators "lend" their stake to validators, as a show of faith in the good behavior of the validator.

## __Nominator__

Nodes which select a set of validators.  A certain amount of DOTs must be staked in order to do so.

## __On-chain governance__

Governance of a blockchain which is controlled by mechanisms controlled by the blockchain.  On-chain governance allows for decisions can be made in a transparent manner.  Note that there are a variety of different algorithms for making these decisions, such as simple majority voting or identity-based quadratic voting.

## __Parachain__

A blockchain which meets several characteristics which allow it work within the confines of the Polkadot Runtime Environment.

## __Parachain Registry__ 

A relatively simple database-like construct that holds both static and dynamic information on each chain.

## __Parity__

A company, founded by Dr. Gavin Wood, which is developing Substrate.  It has also released several other projects including Parity Ethereum and Parity Wasm.

## __Polkadot__

A heterogenous multi-chain technology allowing for various blockchains of different characteristics to perform interchain communication.

## __Polkadot Runtime Environment__

The runtime environment which a runtime module can be executed in.  Parachains must support the Polkadot Runchain Environment - external chains which do not will have to use a bridge.

## __Proof of Stake (PoS)__

A method of achieving consensus in which the next block is determined by a node that is chosen by some characteristic (e.g., the amount of tokens that they stake).

## __Proof of Work__

A method of achieving consensus in which the next block is determined by the first to solve a difficult puzzle (e.g., in Bitcoin, solving a partial pre-image hash for a block candidate).

## __Proposal__

A potential function call to be voted on in a referendum.  Proposals modify the behavior of the Polkadot network, from minor parameter tuning all the way up to replacing the runtime code.

## __Referendum__

A vote on whether or not a proposal should be accepted by the network.  These referenda may be initiated by the Governance Council, by a member of the public, or as the result of a previous proposal.  Stakeholders vote on referenda, weighted by both the size of their stake (i.e. number of DOTs held) and the amount of time they are willing to lock their tokens.

## __Relay chain__

A chain which coordinates consensus and communication between parachains (and external chains, via bridges).

## __Runtime__

A state transition function which indicates a valid algorithm for determining the state of the next block given the previous block.

## __Runtime Module__

WASM code which encodes a state transition function.

## __Safety__

The property of a distributed system indicating that the system will properly meet all invariants; that is, that nothing "bad" ever happens to the data (such as it being corrupted).

## __Sealing__

The process of adding a block to the relay chain.  Note that finalization is a separate process - blocks are finalized some time after they are sealed (the goal is approximately 10 - 12 seconds).

## __Staking__

"Reserving" tokens (for Polkadot, DOTs) which are put up as "collateral" for a chance to produce a valid block (and thus obtain a block reward).  Validators and nominators (who back validators through NPoS) together stake their DOTs in order to add blocks to the relay chain.

## __State transition function__

A function which describes how the state of a blockchain can be transformed.  For example, it may describe how tokens can be transferred from one account to another.

## __Substrate__

An implementation of the Polkadot Runtime Environment which allows developers to generate parachains which are compatible with the Polkadot relay chain.

## __Transaction__

An individual element of the state transition function of a block, such as moving tokens from one account to another.

## __Validator__

A node which secures the relay chain by staking DOTs, validating proofs from collators on parachains, and determine a consensus along with other validators.

## __Voting__

The process of stakeholders determining whether or not a referendum to implement a specific proposal should pass.  Votes are weighted both by the number of DOTs that the stakeholder account controls and the amount of time they are willing to lock their DOTs up.  Voting may be overridden by the Governance Council if there is unanimous agreement that it not

## __Wallet__

A program which allows one to store, receive, and transmit DOTs or other blockchain-based tokens.

## __Web3 Foundation__

A Switzerland-based foundation which nurtures and stewards technologies and applications in the fields of decentralized web software protocols, particularly those which utilize modern cryptographic methods to safeguard decentralization, to the benefit and for the stability of the Web3 ecosystem.

## __WebAssembly / WASM__

An instruction format for a virtual, stack-based machine.  Polkadot Runtime Modules are compiled to WASM.
