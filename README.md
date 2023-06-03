# Euro stablecoin research

This repository aims to serve as an authorative source of information regarding euro stablecoins. Data in this repository should be objective and not make subjective comments. Users of the data may add their own commentary.


## How to contribute?

### Add to the dataset

Anyone is free to contribute to this repository by making a pull request. All commits should be include a reference where maintainers can verify the legitimacy of the newly asserted information. Referencing the issuer of stablecoin is generally fine, but third-party sources are preferred where available.

You should add your information to the CONTRIBUTORS.md together with your first PR and disclose any conflict of interest that you may have.

Please follow the established format. If you have suggestions regarding the formatting of data or adding new data sets, please contact Juuso Roinevirta.

### Fact-check the dataset

Some of the information in this dataset will inevitable become outdated and sometimes PRs containing false information will be approved by mistake. You can contribute by fact-checking the information provided in this repo.

If you find a mistake, fork the repo, fix the error, and make a PR to fix the error. You should add your information to the CONTRIBUTORS.md together with your first PR and disclose any conflict of interest that you may have.

### Donate

This data-set is provided free of charge for anyone to utilise. If you'd like to buy me a coffee, you can donate to `roinevirta.eth` or `roinevirta.sol`


## What is the data structure like?

- Empty entries are considered unknown
- Semi-colon (;) is used to separate lists within a cell
- Dot (.) is used as a decimal separator

The first row of a file contains the name of the data point, a description regarding the data point, and the tickers of the stablecoins included. If you want to include a new stablecoin to the data set, add its ticker (sorted in alphabetical order), to a new column. The data will hence be sorted as follows on each of the files: Data point name, data point description, [tickers]

## Data tables

The database includes the following tables:

- CustomerData: includes information related to the customers the issuer serves and the issuer's business model (e.g. information regarding fee structure)
- DeveloperActivityData: information related to developer activity metrics
- IssuerData: information directly related to the issuer and to the regulatory and legal aspects of the issuer and the stablecoin
- MarketCapitalisationData: information about the total number of stablecoins issued
- ReserveData: information related to the backing and the auditing of the backing assets for fiat stablecoins + information regarding the mechanisms of non-fiat stablecoins
- SecurityData: information regarding the technical security practices of the stablecoin
- TokenInformation: information regarding the technical implementation of the token, for example addresses on which the token is implemented at

## Tips

- Editing CSV files in VS Code is extremely prone to mistakes. This extension might help you a bit: https://marketplace.visualstudio.com/items?itemName=janisdd.vscode-edit-csv