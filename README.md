# VotingContract

VotingContract is a Solidity smart contract that allows users to cast votes, end the voting process, and claim rewards. It implements the `require()`, `assert()`, and `revert()` statements to enforce voting rules and handle different scenarios.

## Contract Overview

The `VotingContract` keeps track of the total votes casted, maximum votes allowed, and whether a user has voted or not. It provides functions for casting votes, ending the voting process, and claiming rewards.

### Contract Functions

#### `castVote()`

Allows a user to cast their vote. It performs the following checks:

- Ensures that the user hasn't already voted.
- Verifies that the maximum vote limit hasn't been reached.

After successful validation, the user's vote is recorded, and the total vote count is incremented.

#### `endVoting()`

Ends the voting process. It performs the following checks:

- Verifies that the total votes casted meets the maximum voting threshold.

Upon successful validation, the end voting logic is executed.

#### `claimReward()`

Allows a user to claim their reward after voting. It performs the following checks:

- Ensures that the user has casted their vote.
- Verifies that the minimum voting threshold has been reached.

Upon successful validation, the reward claiming logic is executed.

### Contract Events

The `VotingContract` emits the following events:

- `VoteCasted`: Triggered when a user casts their vote.
- `VotingCompleted`: Triggered when the voting process is completed, providing the total number of votes casted.

## Usage

To use the `VotingContract`, follow these steps:

1. Deploy the contract on a compatible Ethereum network.
2. Interact with the contract using a compatible wallet or DApp to perform the following actions:
   - Cast votes using the `castVote()` function.
   - End the voting process using the `endVoting()` function.
   - Claim rewards using the `claimReward()` function.

## Author

 Aditya singh

## License

The VotingContract is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
