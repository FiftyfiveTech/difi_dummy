<img src="https://www.fiftyfivetech.io/wp-content/uploads/2021/05/logo.png">

# Difi Dummy Sample

This is a stacking difi application which helps user to stack `mDai` token and earn `Dapp` token when issued based on there stacking.

✨ This repository showing that how we are using clean code architecture, folder structure, and component reusability.✨

We at Fiftyfive Technologies follow the practices defined by SOLID principles and Clean Architecture.

## Features

- _**Functionality**_  : Work correctly, efficiently, and robustly.
- _**Readability**_    : The primary audience for our code is other developers.
- _**Extensibility**_  : Well-designed code should be extensible as a building block for solving new problems.
- _**Scalability**_    : The code that can scale along with the need of your business.

## Tech Stack

- [NodeJS](https://nodejs.org/en/) - JS runtime environment
- [Truffle Suite](https://trufflesuite.com/) - Web3 development framework on top of node.
- [Ganache](https://trufflesuite.com/ganache/) - For local web3 environment to maintain dev/testing blockchain. 
- [Metamask](https://metamask.io/) - For decentralised crypto wallet.
- [Solidity](https://soliditylang.org/) - To generate smart contracts.
- [React](https://reactjs.org/) - To create a supporting frontend
- [Chai](https://www.chaijs.com/) - JS based testing framework.

## Package manager - npm

This project is using `npm` as package manager, if you do not have this installed on your machine please start by looking at the [npm docuentation and tutorials](https://docs.npmjs.com/). After installing the package manager the following commands will be availible for you:
- `npm install` - Installing dev dependencies.
- `npm run start:local` - To start the sever.

If you seem to still have issues with these commands, try running `npm cache clean` and do `npm install` or `npm install --legacy-peer-deps`

## Linting

Project is using ESLint to make sure that we keep same coding style in the project. Currently the project is using default ruleset, but custom can be defined in `.eslintrc.json`.


# How to use this package

To use this package, enter this simple command on your `Terminal` or any other tool that can run `npm` commands.

To install package dependencies
```sh
npm install
```

To compile the project
```sh
truffle compile
```

To start unit testing
```sh
truffle test
```

To migrate/deploy contract
```sh
truffle migrate
```

To start front-end
```sh
npm run start
```

To run script / issue token (when user have stack some `mDai`)
```sh
truffle exec scripts/issue-token.js
```

# Project Architecture and Structure

### Architecture

![image](https://user-images.githubusercontent.com/95676326/208651850-15ecc661-ee74-4f07-82e9-56d49468fe41.png)

### Structure

```
├───migrations/
│   ├───1_initial_migration.js
│   └───2_deploy_contracts.js
├───public/
│   ├───favicon.ico
│   ├───index.html
│   └───manifest.json
├───scripts/
│   └───issue-token.js
├───src/
│   ├───abis/
│   │   ├───DaiToken.json
│   │   ├───DappToken.json
│   │   ├───Migrations.json
│   │   └───TokenFarm.json
│   ├───components/
│   │   ├───App.css
│   │   ├───App.js
│   │   ├───Main.js
│   │   └───Navbar.js
│   ├───contracts/
│   │   ├───DaiToken.sol
│   │   ├───DappToken.sol
│   │   ├───Migrations.sol
│   │   └───TokenFarm.sol
│   ├───index.js
│   └───serviceWorker.js
├───test/
│   └───TokenFarm.test.js
├───.babelrc
├───.gitignore
├───Readme.md
├───package.json
└───truffle-config.js
```
**src/contracts** - Contains the solidity contract for stacking managing wallets and token farming with all different contract.

**src/abis** - It contain json file generated on compiling contract which help us to intract with contract's methods.

**src/components** -  It consist of files that intract with smart-contract and wallets using `web3` and makes all the flow with UI.

**migrations** - Migration file is for deploying and migrating contract to configured web3 network.

**test** - Using `chai` as testing framework for writing test cases and run test suit for the contract that are generated in `src/contracts` directory with help of abis on the respective contracts.

**scripts** - It it scripts of command that issue valued token to user based on there stacking mDai amount.

## License

Fiftyfive Technologies

**We are relentlessly focusing on digital transformation. Dive deep into the customer cases to know more about the project which we delivered.**

