# Forta Labelled Datasets

Publicly available datasets of suspicious Web3 activity is limited on all Forta supported chains. Without this, it can be a challenge to create or evaluate machine-learning based solutions.

Inspired by https://cryptoscamdb.org/ and https://www.web3rekt.com/ that keeps track of crypto scams in an open source database, this repository aims to maintain and share Web3 threat related datasets with the Forta community. Contributions are welcome!

## Malicious Smart Contracts

### Datasets

| 🗂 Filepath | ⛓ Chain | 📝 Description |
|---|---|---|
| `labels/1/malicious_smart_contracts.csv`  | Ethereum Mainnet  | Smart contracts deployed on Ethereum Mainnet (chainId: 1). Data was extracted from the following sources: <ul><li>[Luabase](https://luabase.com) `ethereum.tags` table: malicious addresses with etherscan labels `exploit`, `heist`, and `phish-hack`</li><li>🛠Coming soon!🛠: More DeFi hacks</li></ul> |
| `labels/10/malicious_smart_contracts.csv`  | Optimism  | Smart contracts deployed on Optimism (chainId: 10). Data was extracted from the following sources: <ul><li>Malicious addresses with optimistic.etherscan label `exploit`</li></ul> |

### Schema

CSV files with the name `malicious_smart_contracts.csv` will have the following columns:

| Column | Description   |
|---|---|
| contract_address  | smart contract address involved in exploits/heist/phish  |
| contract_tag  | smart contract tag from etherscan  |
| contract_creator  | smart contract's deployer address  |
| contract_creation_tx  | smart contract creation tx hash  |
| contract_creator_tag  | smart contract's deployer from etherscan  |
| source  | where the date came from  |
| notes  | any additional notes  |
| contract_creator_etherscan_label  | etherscan labels for contract_creator address |

## Phishing Scams

### Datasets

| 🗂 Filepath | ⛓ Chain | 📝 Description |
|---|---|---|
| `labels/1/phishing_scams.csv`  | Ethereum Mainnet  | Addresses involved in phishing scams. Data was extracted from the following sources: <ul><li>[Luabase](https://luabase.com) `ethereum.tags` table: malicious addresses with etherscan labels `phish-hack`</li><li>🛠Coming soon!🛠: Phishing scams from [Chainabuse](https://www.chainabuse.com/)</li></ul> |

### Schema

CSV files with the name `phishing_scams.csv` will have the following columns:

| Column | Description   |
|---|---|
| address  | address involved in phishing scam  |
| is_contract  | boolean flag whether address is a contract or EOA  |
| etherscan_tag  | address tag from etherscan  |
| etherscan_labels  | etherscan labels for address  |

## Malicious Addresses

### Datasets

| 🗂 Filepath | ⛓ Chain | 📝 Description |
|---|---|---|
| `labels/1/etherscan_malicious_labels.csv`  | Ethereum Mainnet  | Addresses with etherscan labels `exploit`, `heist`, and `phish-hack`(chainId: 1). |