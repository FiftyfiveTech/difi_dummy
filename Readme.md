<img src="https://www.fiftyfivetech.io/wp-content/uploads/2021/05/logo.png">

# Difi Dummy Sample

This is a stacking difi application which help user to stack mDai token and earn Dapp token when issued based on there stacking.

# Prerequisite
- You should following installed on your system:
    - `Node`
    - `Ganche`
    - `Truffle`
    - `Metamask`

# How to use this package

To use this package and fetch a template of your choosing, enter this simple command on your `Terminal` or `GitBash` or any other tool that can run `npm` commands.

To get package
```sh
npm install
```

To compile
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

# Project structure

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

## Contribute

* Fork repository. ✌️
* Add your feature 😎 or fix a 🐛.
* Raise a pull request. 🤓

## Author

Fiftyfive Technologies
