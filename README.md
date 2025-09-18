# Bank Smart Contract Project

This project demonstrates a simple Ethereum smart contract for a basic bank, built with Solidity and deployed using Hardhat.

## Project Structure

- [`contracts/Bank.sol`](contracts/Bank.sol): The main smart contract source code.
- [`scripts/deploy.js`](scripts/deploy.js): Script to deploy the Bank contract.
- [`hardhat.config.js`](hardhat.config.js): Hardhat configuration, including network settings.
- [`test/`](test/): Directory for test scripts.
- [`ignition/modules/`](ignition/modules/): Hardhat Ignition deployment modules.
- [`artifacts/`](artifacts/): Compiled contract artifacts (auto-generated).
- [`cache/`](cache/): Hardhat cache files (auto-generated).

## Bank Contract

The [`Bank`](contracts/Bank.sol) contract allows users to deposit and withdraw Ether. Each user's balance is tracked in a mapping.

### Functions

- `deposit()`: Deposit Ether into your account.
- `withdraw(uint256 _amount)`: Withdraw a specified amount of Ether from your account.

## Deployment

The Bank contract has been deployed to the following address:

```
0xA5f1695a08E0EEAee4909F4AfE32b8d6e1F84fff
```

### Deploying Locally

1. Install dependencies:

   ```sh
   npm install
   ```

2. Set your private key in a `.env` file:

   ```
   PRIVATE_KEY=your_private_key_here
   ```

3. Deploy to the configured network:

   ```sh
   npx hardhat run scripts/deploy.js --network coretestnet
   ```

## Hardhat Tasks

Try running some of the following tasks:

```sh
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat ignition deploy ./ignition/modules/Lock.js
```

## Requirements

- Node.js
- Hardhat
- An Ethereum wallet private key (for deployment)

## License

MIT
