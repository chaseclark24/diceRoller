# Nebulas Dice Roller

A historical decentralized application that generated an arbitrary-sided die roll and recorded the result on the Nebulas blockchain.

> **Status:** Historical source only. [Nebulas ended its mainnet service](https://www.nebulas.io/) in December 2024, so the original application can no longer complete live blockchain transactions.

## How it worked

1. The user selected the number of sides for the die.
2. The browser loaded and unlocked a Nebulas wallet file locally.
3. The frontend signed a transaction calling `xSideRoll` on the smart contract.
4. The contract generated a result and stored the number of sides, result, and timestamp under the transaction hash.
5. The frontend used that hash to retrieve and display the recorded roll.

The contract rejected attached donations, so users paid only the network gas fee.

## Important files

- `diceRoller.js` — Nebulas smart contract.
- `index.html` — original dApp interface and transaction flow.
- `server.js` — small local static server used during development.
- `lib/` and `js/` — bundled Nebulas wallet and browser dependencies.

## Technology

- JavaScript
- Nebulas smart contracts
- Nebulas JavaScript SDK
- HTML and Bootstrap

## Historical note

This repository is retained to show the original contract and browser integration. The included wallet utilities and network endpoints are obsolete and should not be used to create or import a current cryptocurrency wallet.
