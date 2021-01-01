### Chapter X

# 👨‍🌾 EthBuilders Yield Farming - IN PROGRESS

Learn about yield farming by building a farm in a hands-on manner.

## About EthBuilders

Our purpose is to provide the best open source materials to learn Ethereum development in-depth.

A special thanks to [ConsenSys Developer Portal](https://consensys.net/developers/) and [Dapp University](https://www.dappuniversity.com/).

## Table of Contents

<!-- TOC -->
- [👨‍🌾 EthBuilders Yield Farming - IN PROGRESS](#-ethbuilders-yield-farming---in-progress)
  - [About EthBuilders](#about-ethbuilders)
  - [Table of Contents](#table-of-contents)
  - [What is Yield Farming?](#what-is-yield-farming)
    - [History](#history)
    - [How does it work?](#how-does-it-work)
      - [Staking](#staking)
  - [Project Setup](#project-setup)
    - [Installing NodeJS](#installing-nodejs)
    - [Creating the Folder](#creating-the-folder)
    - [Set Up package.json](#set-up-packagejson)
    - [Installing Truffle And its Dependencies](#installing-truffle-and-its-dependencies)
      - [What is Truffle?](#what-is-truffle)
      - [Installing locally vs globally](#installing-locally-vs-globally)
      - [Install Truffle](#install-truffle)
      - [Installing Ganache](#installing-ganache)
      - [Initalize Truffle a Project](#initalize-truffle-a-project)
    - [Quick Start Setup](#quick-start-setup)
  - [Understanding the Project Structure](#understanding-the-project-structure)
  - [Truffle Project Structure](#truffle-project-structure)
    - [Overview of package.json](#overview-of-packagejson)
      - [What is package-lock.json?](#what-is-package-lockjson)
      - [What is node_modules](#what-is-node_modules)
    - [Configurations with truffle.config.js](#configurations-with-truffleconfigjs)
    - [Contracts and Migrations](#contracts-and-migrations)
    - [Overview of Migrations Scripts](#overview-of-migrations-scripts)
    - [Tests and Test Driven Development](#tests-and-test-driven-development)
      - [Security and The Importance of Tests](#security-and-the-importance-of-tests)
      - [./test](#test)
<!-- /TOC -->

## What is Yield Farming?

👨‍🌾 Yield Farming is ....

Yield can be defined as ...

It is also known as "liquidity mining".

Liquidity is defined as ...

Staking is defined as ...

Yield farming and staking are two sides of the same coin

### History

Yield Farming was first created by [Synthetix](https://www.synthetix.io/), a derivatives liquidity protocol. It was later popularized by [Compound Finance](https://compound.finance/), a lending desk protocol and [Balancer](https://balancer.finance/), a protocol for programmable liquidity.

### How does it work?

Yield Farming is a way to direct capital to active network members who are building the protocol, instead of relying on mere [airdrops]().

It can be considered a growth hack as it is designed to incentivize liquidity on a protocol. This brings in suppliers and users.

#### Staking

To gain a yield one has to stake.

## Project Setup

- [ ] Install NodeJS
- [ ] Create a folder for the project
- [ ] Install Truffle
- [ ] Initialize a Truffle workplace

Want a quick setup? Go click on [Quick Start Setup](#quick-start-setup)

### Installing NodeJS

NodeJS is the preferred runtime environment to create develop DApps.  

It comes with [npm](https://www.npmjs.com/), node's package manager. With npm, we can install all sort of programs and code snippets developed by the community to make our lives easier.

Make sure you have NodeJS installed.  

The follow command checks for NodeJS on your system.  

`node -v`

<details> <summary>See output</summary>

```sh
$ node -v
v10.17.0
```
</details>

<br />

> Any version above v10.0 will do

If you don't see Node on your system:

1. Go to the [website](https://nodejs.org/en/)
2. Install the long term support version (LTS).

<br/>

### Creating the Folder

Create a folder for your project and enter the folder.  

```sh
$ mkdir yield-farm
$ cd yield-farm
```
<br/>

### Set Up package.json

To install Truffle and any project dependencies, we first have to intialize a `package.json` file.

`package.json` stores your dependencies in the  `/node modules` directory.

Check that you are in the project folder.
> pwd means print working directory, the root directory your terminal is in.
  
```sh
$ pwd
```

<details> <summary>See output</summary>

```sh
$ pwd
/YOUR/ABSOLUTE/PATH/VARIES/yield-farm
```

</details>

<br />

In the root of your folder, initialize npm and create a package.json file.  
> The `-y` flag allows the quick setup of a default package.json without all the usual setup questions.  
> You can go back and fill in the fields if you'd like.  

```sh
$ npm init -y
```

<details> <summary>See output</summary>

```sh
$ npm init -y
Wrote to /YOUR/ABSOLUTE/PATH/VARIES/yield-farm/package.json:

{
  "name": "yield-farm",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

</details>

<br />

### Installing Truffle And its Dependencies

#### What is Truffle?

[Truffle](https://www.trufflesuite.com/) is an environment that to develop DApps and smart contracts on Ethereum.

Or as the website states, its a "world class development environment, testing framework and asset pipeline for blockchains using the Ethereum Virtual Machine (EVM), aiming to make life as a developer easier".

#### Installing locally vs globally

We will be installing all of our `/node modules` into the local project. It is recommended to install locally instead of globally, because tools in the Ethereum ecosysetm change quickly.

#### Install Truffle

To install Truffle run the following command

```sh
$ npm install truffle@5.1.59 --save-dev
```

> --save-dev installs truffle as a dev dependencies  

> truffle@5.1.59 installs that specific package version  
> Having the same version reduces the chance that a truffle update  
> creates a breaking change that may cause issues

<details> <summary>See output</summary>

```sh
$ npm install truffle@5.1.59 --save-dev

> truffle@5.1.59 postinstall /YOUR/ABSOLUTE/PATH/VARIES/yield-farm/node_modules/truffle
> node ./scripts/postinstall.js

- Fetching solc version list from solc-bin. Attempt #1
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN yield-farm@1.0.0 No description
npm WARN yield-farm@1.0.0 No repository field.

+ truffle@5.1.59
added 144 packages from 66 contributors and audited 144 packages in 31.025s

37 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

</details>

<br/>

#### Installing Ganache

Next we install Ganache, a tool to test our project on a local Ethereum blockchain.

Ganache comes in two flavors:
1. [Ganache-cli](https://github.com/trufflesuite/ganache-cli) - a command line interface
2. [Ganache GUI](https://www.trufflesuite.com/ganache) - a graphical user interaface

For this project will be using the Ganache-cli. If you'd like, you can install both.
Again we will install the tool locally as a `dev dependency` as opposed to global.

> A `dev dependency` is a module of code that is not used in the app directly, but used to support development.

To install Ganache-cli we run:

```sh
$ npm install ganache-cli@6.12.1 --save-dev
```

<details> <summary>See output</summary>

```sh
$ npm install ganache-cli@6.12.1 --save-dev

> keccak@3.0.1 install /Users/anthonyalbertorio/Code/ethDev/yield-farm/node_modules/ganache-cli/node_modules/keccak
> node-gyp-build || exit 0


> secp256k1@4.0.2 install /Users/anthonyalbertorio/Code/ethDev/yield-farm/node_modules/ganache-cli/node_modules/secp256k1
> node-gyp-build || exit 0

npm WARN yield-farm@1.0.0 No description
npm WARN yield-farm@1.0.0 No repository field.

+ ganache-cli@6.12.1
added 101 packages from 182 contributors and audited 245 packages in 5.82s

37 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

```
</details>

<br/>

To Install Ganache GUI, go to [their website](https://www.trufflesuite.com/ganache) and follow the instructions. The GUI will allow you to have an interactive desktop app that runs your local Ethereum blockchain.

#### Initalize Truffle a Project

To initialize a Truffle project run the following command

```sh
$ truffle init
```

> `Truffle init` sets up the project structure for your project

<details> <summary>See output</summary>

```sh
$ truffle init

Starting init...
================

> Copying project files to /YOUR/ABSOLUTE/PATH/VARIES/yield-farm

Init successful, sweet!
```
</details>

<br/>

Success! We have Installed all our initial dependenices and setup the project!

### Quick Start Setup
If you want to quickly set up a project, folow the instructions below.

1. Check to have NodeJS v10.0 or higher. Or install it.
2. Navigate into a directory to create your repo
3. Follow commands below

```sh
$ mkdir yield-farm
$ cd yield-farm
$ npm init - y
$ npm install truffle@5.1.59 --save-dev
$ npm install ganache-cli@6.12.1 --save-dev
$ truffle init
$ touch .gitignore
```

<br/>

## Understanding the Project Structure

We now have the basic ingredients for a Truffle Project.

We will explain the following parts:

- [ ] the Truffle Project Structure
- [ ] `package.json`
- [ ] `package-lock.json`
- [ ] `/node_modules`
- [ ] `truffle.config.js` and configuration
- [ ] `/contracts` and Migrations.sol Contract
- [ ] `/migrations` and migration scripts
- [ ] `/tests` and testing

Don't be intimidated. The files have very simple functions. 😃

<br/>

## Truffle Project Structure

Thanks to running `truffle init` command, we created the scaffolding to build our project.

This is the basics to get started. Below is a description of each part and what it does.

```
├──contracts
│    └──Migrations.sol
├──migrations
│   └──1_initial_migration.js
├──node_modules
│   └──VARIOUS SUB-FOLDERS
├──test
├──package-lock.json
├──package.json
├──.gitignore
└──truffle-config.js
```

<br/>

### Overview of package.json
`package.json` is the file that lists our dependencies for our project.
It is also used for defining project properties, description, author & license information, scripts, etc.

Whenever we install something using npm, it is listed here. That way other devs can download our project and run `npm i` and install the same modules. We do not need to commit our `./node_modules` folder
to our github repos.

See the [package.json npm documentation](https://docs.npmjs.com/cli/v6/configuring-npm/package-json) for more information.

<br/>

#### What is package-lock.json?
`package-lock.json` is solely used to lock dependencies to a specific version number. Since dependencies can have version updates.  If included in a project, `package-lock.json` get the exact version during installation.

It is automatically generated for any operations where npm modifies either the `node_modules` tree, or `package.json`.

See the [package-lock.json npm documentation](https://docs.npmjs.com/cli/v6/configuring-npm/package-lock-json) for more information.

<br/>

#### What is node_modules
`./node_modules` is the directory where all our dependencies go when we install them via npm.

The main important thing to know is: **NEVER MODIFY ANY FILES OR FOLDERS INSIDE OF NODE MODULES**

Why? Its a poor practice. Your `./node_modules` files will be different than what others download via npm. It will inevitably cause bugs and issues. This is a general rule that applies to any projects using NodeJS or npm.

<br/>

### Configurations with truffle.config.js

<br/>

### Contracts and Migrations

<br/>

### Overview of Migrations Scripts

<br/>

### Tests and Test Driven Development

#### Security and The Importance of Tests

#### ./test
