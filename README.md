<p align="center">
    <h1 align="center">
        InterRep contracts
    </h1>
    <p align="center">InterRep Solidity smart contracts.</p>
</p>

<p align="center">
    <a href="https://github.com/InterRep" target="_blank">
        <img src="https://img.shields.io/badge/project-InterRep-blue.svg?style=flat-square">
    </a>
    <a href="https://eslint.org/" target="_blank">
        <img alt="Linter eslint" src="https://img.shields.io/badge/linter-eslint-8080f2?style=flat-square&logo=eslint">
    </a>
    <a href="https://prettier.io/" target="_blank">
        <img alt="Code style prettier" src="https://img.shields.io/badge/code%20style-prettier-f8bc45?style=flat-square&logo=prettier">
    </a>
    <img alt="Repository top language" src="https://img.shields.io/github/languages/top/InterRep/contracts?style=flat-square">
</p>

<div align="center">
    <h4>
        <a href="https://docs.interrep.link/contributing">
            👥 Contributing
        </a>
        <span>&nbsp;&nbsp;|&nbsp;&nbsp;</span>
        <a href="https://docs.interrep.link/code-of-conduct">
            🤝 Code of conduct
        </a>
        <span>&nbsp;&nbsp;|&nbsp;&nbsp;</span>
        <a href="https://t.me/interrep">
            🗣️ Chat &amp; Support
        </a>
    </h4>
</div>

---

If you want an overwiew of InterRep, read our announcement post: https://jaygraber.medium.com/introducing-interrep-255d3f56682. For more details, please see our [documentation website](https://docs.interrep.link).

⚠️ **Notice**: [interrep.link](https://interrep.link) and [ropsten.interrep.link](https://ropsten.interrep.link) still refer to the old MVP version of interRep. They will soon be updated. You can find an updated version at [kovan.interrep.link](https://kovan.interrep.link) (staging env).

### Deployed contracts

|                           | Kovan                                                                                           | Ropsten                                                                                          | Arbitrum One                                                                                          |
| ------------------------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| ReputationBadge (Twitter) | [0x0Cb0....1EB6](https://kovan.etherscan.io/address/0x0Cb09b04016Ba1CfBF37359f0112F304F2381EB6) | [0x2F4d...BC11](https://ropsten.etherscan.io/address/0x2F4d1333337b5C4C47Db5DB3A36eD547a549BC11) | [0x2F4d...BC11](https://explorer.offchainlabs.com/address/0x2F4d1333337b5C4C47Db5DB3A36eD547a549BC11) |
| ReputationBadge (Github)  | [0xab00...73bf](https://kovan.etherscan.io/address/0xab0090f2F9C061C12D3Fa286079659Fe00e173bf)  |                                                                                                  |                                                                                                       |
| ReputationBadge (Reddit)  | [0xAB18...6c37](https://kovan.etherscan.io/address/0xAB1855a7d02C771465411fDD4B63f647925d6c37)  |                                                                                                  |                                                                                                       |
| InterRepGroups            | [0xB9A5...a1E4](https://kovan.etherscan.io/address/0xB9A55B681BF8426ceb71F54d127D3391fd28a1E4)  | [0xa2A7...6419](https://ropsten.etherscan.io/address/0xa2A7f256B4Ea653eef95965D09bbdBb4b4526419) |                                                                                                       |

---

## Install

Clone this repository and install the dependencies:

```bash
$ git clone https://github.com/InterRep/contracts.git interrep-contracts
$ cd interrep-contracts
$ yarn # or `npm i`
```

## Usage

### Compile

Compile the smart contracts with Hardhat:

```bash
$ yarn compile
```

This should generate the TypeChain typings. If you want to generate them manually run:

```bash
$ yarn typechain
```

### Lint

Lint the Solidity or the TypeScript code:

```bash
$ yarn lint:sol
$ yarn lint:ts
# or yarn lint to lint both.
```

And check if the code is well formatted:

```bash
$ yarn prettier
```

### Test

Run the Mocha tests:

```bash
$ yarn test
```

### Coverage

Generate the code coverage report:

```bash
$ yarn coverage
```

### Report Gas

See the gas usage per unit test and average gas per method call:

```bash
$ REPORT_GAS=true yarn test
```

### Clean

Delete the smart contract artifacts, the coverage reports and the Hardhat cache:

```bash
$ yarn clean
```

### Deploy

Deploy the contracts to Hardhat Network:

```bash
$ yarn deploy:reputation-badge --name "InterRep Twitter Badge" --symbol iTWITT
$ yarn deploy:interrep-groups
```

or run `yarn deploy:mocks` if you want a short command to simulate the previous command for testing purposes.

Set your `.env` file and deploy the contracts to a specific network, such as the Ropsten testnet:

```bash
$ NODE_ENV=production yarn deploy:reputation-badge --name "InterRep Twitter Badge" --symbol iTWITT --network ropsten
$ NODE_ENV=production yarn deploy:interrep-groups --network ropsten
```

You can find a copy of the `.env` file in the `.env.example` file.

## Syntax Highlighting

If you use VSCode, you can enjoy syntax highlighting for your Solidity code via the
[vscode-solidity](https://github.com/juanfranblanco/vscode-solidity) extension. The recommended approach to set the
compiler version is to add the following fields to your VSCode user settings:

```json
{
    "solidity.compileUsingRemoteVersion": "v0.8.4+commit.c7e474f2",
    "solidity.defaultCompiler": "remote"
}
```

Where of course `v0.8.4+commit.c7e474f2` can be replaced with any other version.
