# Euro stablecoin research

This repository aims to serve as an authorative source of information regarding euro stablecoins. Data in this repository should be objective and not make subjective comments. Users of the data may add their own commentary.

Please note that we distinguish between tokens and issuers. One issuer may issue many tokens and they may be regulated under different rules or be otherwise materially different.


## How to contribute?

### Add to the dataset

Anyone is free to contribute to this repository by making a pull request. All commits should be include a reference where maintainers can verify the legitimacy of the newly asserted information. Referencing the issuer of stablecoin is generally fine, but third-party sources are preferred where available.

You should add your information to the Contributors.csv together with your first PR and disclose any conflict of interest that you may have.

Please follow the established format. If you have suggestions regarding the formatting of data or adding new data sets, please contact Juuso Roinevirta.

### Fact-check the dataset

Some of the information in this dataset will inevitable become outdated and sometimes PRs containing false information will be approved by mistake. You can contribute by fact-checking the information provided in this repo.

If you find a mistake, fork the repo, fix the error, and make a PR to fix the error. You should add your information to the CONTRIBUTORS.md together with your first PR and disclose any conflict of interest that you may have.

### Donate

This data-set is provided free of charge for anyone to utilise. If you'd like to buy me a coffee, you can donate to `roinevirta.eth` or `roinevirta.sol`

## Contributors

You can find a list of contributors to this data set from the `Contributors.csv`. This is a list of contributors to this repository and research. It also serves as a resource to check conflicts of interest to ensure the objectivity of data.

*Contributors: please add your information in this file together with your first PR. Your role should be Contributor.*

Roles
- Contributors: research, add data, make pull requests
- Maintainers: fact-check and approve pull requests

**A big thank you to all the contributors**


## What is the data structure like?

- Empty entries are considered unknown
- Semi-colon (;) is used to separate lists within a cell
- Dot (.) is used as a decimal separator
- Dot may be used to categorise data point names (e.g. two data points related to the CEO could be `CEO.Name` & `CEO.Age`)

The first row of a file contains the name of the data point, the second a description regarding the data point, the third a description of which type of data is expected in the cell. Stablecoin data then starts from the fourth row. To add a new stablecoin, simply add a new row to all the relevant data tables.

## Data tables

The database includes the following tables:

- `Contributors`: list of people who have contributed to this data set
- `DeveloperActivityData`: information related to developer activity metrics
- `IssuerData`: information directly related to the issuer and to the regulatory and legal aspects of the issuer
- `MarketCapitalisationData`: information about the total number of stablecoins issued
-- Market cap is calculated as tokens issued less unreleased tokens less blocklisted tokens. Excludes bridged tokens.
-- XTotal is the sum of all the other market caps provided
- `ReserveData`: information related to the backing and the auditing of the backing assets for fiat stablecoins + information regarding the mechanisms of non-fiat stablecoins
- `ServiceData`: includes information related to the issuer's services, customers the issuer serves, and the issuer's business model (e.g. information regarding fee structure)
- `TechnicalTokenInformation`: information regarding the technical implementation of the token, for example addresses on which the token is implemented at
- `TokenInformation`: information regarding the non-technical characteristics of the token (not issuer, for issuer information, see IssuerData)

### Metadata tables

Metadata tables provide information about the source, date, and person adding the information. They follow exactly the same format as their non-metadata counterpart; for example the metadata cell at (3,3) corresponds to the data in cell (3,3) in the original data table.

Metadata tables are available in the `metadata` directory.

Metadata tables contain information in the following format: `[[person,date,source],[person,date,source]]`
- `person` is the github username of the person who made the latest edit
- `date` is the date at which the source of data was accessed (in YYYYMMDD format)
- `source` is the URL from which the data was obtained. For offline data this is an APA style reference.

If more than one people corrobarate the same data point, the second person should add their entry to the list of lists.

Examples:
- One person adds a metadata source: `[[roinevirta;20231006;https://google.com]]`
- The person finds another source that supports the information: `[[roinevirta;20231006;https://google.com];[roinevirta;20231007;http://wikipedia.org]]`
- Second person finds another source that supports the claim: `[[roinevirta;20231006;https://google.com];[roinevirta;20231007;http://wikipedia.org];[githubuser;20231028;Sapolsky, R. M. (2017). Behave: The biology of humans at our best and worst. Penguin Books.]]`


### Blockchain abbreviations used

We use abbreviations to refer to blockchains. Below are some of the abbreviations:

**Mainnets**
- `Algorand`: Algorand
- `ArbitrumNova` Arbitrum Nova
- `ArbitrumOne`: Arbitrum One
- `AvalancheCChain`: Avalanche C-Chain
- `BinanceSmartChain`: Binance Smart Chain
- `Celo`: Celo
- `Ethereum`: Ethereum
- `Fantom`: Fantom
- `Gnosis`: Gnosis
- `Omni`: Omni
- `Optimism`: Optimism
- `Polygon`: Polygon
- `Solana`: Solana
- `Tezos`: Tezos
- `Tron`: Tron

**Testnets**
- `ArbitrumOneGoerli`: Arbitrum One Goerli
- `AvalancheFuji`: Avalanche Fuji
- `EthereumGoerli`: Ethereum Goerli
- `EthereumSepolia`: Ethereum Sepolia
- `GenXTestnet`: GEN-X Testnet for Gaia-X Web3 ecosystem
- `PolygonMumbai`: Polygon Mumbai
- `SolanaDevnet`: Solana Devnet

*Contributors: please use the abbreviations exactly. If you are adding a new network, please add its abbreviation here.*

## Tips

- Editing CSV files in VS Code is extremely prone to mistakes. This extension might help you a bit: https://marketplace.visualstudio.com/items?itemName=janisdd.vscode-edit-csv