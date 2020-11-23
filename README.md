# mirrorcli <!-- omit in toc -->

Command-line interface for Mirror Protocol on Terra.

## Table of Contents <!-- omit in toc -->

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
  - [Execute](#execute)
  - [Query](#query)
- [License](#license)

## Installation

**Requirements**

- Node.js 12+
- NPM
- (`terracli`)[https://github.com/terra-project/core] in your path

`mirrorcli` can be through off NPM.

```bash
$ npm install -g @mirror-protocol/mirrorcli
```

The entrypoint `mirrorcli` should then be available in your `path`:

<pre>
        <div align="left">
        <strong>$ mirrorcli</strong>

        Usage: mirrorcli [options] [command]

        Command-line interface for interacting with Mirror Protocol on Terra

        Options:
          -V, --version   output the version number
          -v,--verbose    Show verbose error logs
          -h, --help      display help for command

        Commands:
          exec|x          Execute a function on a smart contract
          query|q         Run a smart contract query function
          help [command]  display help for command
        </div>
</pre>

## Configuration

`mirrorcli` will create a configuration file in your home directory: `$HOME/.mirrorclirc.json`.

## Usage

`mirrorcli` allows you to:

- [**execute**](#execute) state-changing functions on Mirror and Terraswap smart contracts
- [**query**](#query) readonly data endpoints on Mirror and Terraswap smart contracts

### Execute

**USAGE: `mirrorcli exec|x [options] [command]`**

```
Execute a function on a smart contract

Options:
  --yaml                        Encode result as YAML instead of JSON
  -y,--yes                      Sign transaction without confirming (yes)
  --home <string>               Directory for config of terracli
  --from <string>               *Name of key in terracli keyring
  --generate-only               Build an unsigned transaction and write it to stdout
  -b,--broadcast-mode <string>  Transaction broadcasting mode (sync|async|block) (default: sync) (default: "sync")
  --chain-id <string>           Chain ID of Terra node
  -a,--account-number <int>     The account number of the signing account (offline mode)
  -s,--sequence <int>           The sequence number of the signing account (offline mode)
  --memo <string>               Memo to send along with transaction
  --fees <coins>                Fees to pay along with transaction
  --gas <int|auto>              *Gas limit to set per-transaction; set to "auto" to calculate required gas automatically
  --gas-adjustment <float>      Adjustment factor to be multiplied against the estimate returned by the tx simulation
  --gas-prices <coins>          Gas prices to determine the transaction fee (e.g. 10uluna,12.5ukrw)
  -h, --help                    display help for command

Commands:
  collector [options]         Mirror Collector contract functions
  factory [options]           Mirror Factory contract functions
  gov [options]               Mirror Gov contract functions
  mint [options]              Mirror Mint contract functions
  oracle [options]            Mirror Oracle contract functions
  staking [options]           Mirror Staking contract functions
  mirror-token|MIR [options]  Mirror Token contract functions
  terraswap|ts [options]      Terraswap contract functions
  help [command]              display help for command
```

### Query

**USAGE: `mirrorcli query|q [options] [command]`**

```
Run a smart contract query function

Options:
  -h, --help                  display help for command

Commands:
  collector [options]         Mirror Collector contract queries
  factory [options]           Mirror Factory contract queries
  gov [options]               Mirror Gov contract queries
  mint [options]              Mirror Mint contract queries
  oracle [options]            Mirror Oracle contract queries
  staking [options]           Mirror Staking contract queries
  mirror-token|MIR [options]  Mirror Token contract queries
  terraswap|ts [options]      Terraswap contract queries
  help [command]              display help for command
```

## License

This software is licensed under the Apache 2.0 license. Read more about it [here](./LICENSE).

© 2020 Mirror Protocol