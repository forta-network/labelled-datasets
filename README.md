# Forta Labelled Datasets

Publicly available datasets of suspicious Web3 activity is limited on all Forta supported chains. Without this, it can be a challenge to create or evaluate machine-learning based solutions.

Inspired by https://cryptoscamdb.org/ and https://www.web3rekt.com/ that keeps track of crypto scams in an open source database, this repository aims to maintain and share Web3 threat related datasets with the Forta community. Contributions are welcome!

## Datasets

### ChainId 1: Ethereum

* `labels/1/malicious_smart_contracts.csv`: Smart contracts deployed on Ethereum Mainnet (chainId: 1). Data was extracted from the following sources:
    * [Luabase](https://luabase.com) `ethereum.tags` table: malicious addresses with etherscan labels `exploit`, `heist`, and `phish-hack`
* `labels/1/phishing_scams.csv`: Addresses involved in phishing scams. Data was extracted from the following sources:
    * [Luabase](https://luabase.com) `ethereum.tags` table: malicious addresses with etherscan labels `phish-hack`


### ChainId 10: Optimism

* `labels/10/malicious_smart_contracts.csv`: Smart contracts deployed on Optimism (chainId: 10). Data was extracted from the following sources:
    * malicious addresses with optimistic.etherscan label `exploit`


## Dataset Schema

### `malicious_smart_contracts`

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

### `phishing_scams`

CSV files with the name `phishing_scams.csv` will have the following columns: coming soon!

| Column | Description   |
|---|---|
| address  | address involved in phishing scam  |
| is_contract  | boolean flag whether address is a contract or EOA  |
| etherscan_tag  | address tag from etherscan  |
| etherscan_labels  | etherscan labels for address  |
