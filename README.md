# AITU_SE2315 ERC20 Token

## Overview
AITU_SE2315 is an ERC20 token implemented using Solidity and OpenZeppelin contracts. The contract supports standard ERC20 functionalities along with additional features such as gasless transactions using `ERC20Permit` and utility functions for querying sender details and timestamps.

## Features
- Implements ERC20 token standards.
- Supports gasless approvals via `ERC20Permit`.
- Includes utility functions for transaction sender and timestamp retrieval.
- Initial supply of 2000 tokens is minted to the contract owner upon deployment.

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [Hardhat](https://hardhat.org/)
- [OpenZeppelin Contracts](https://github.com/OpenZeppelin/openzeppelin-contracts)

### Clone Repository
```sh
git clone https://github.com/your-repo/AITU_SE2315.git
cd AITU_SE2315
```

### Install Dependencies
```sh
npm install
```

## Deployment
To deploy the contract locally:
```sh
npx hardhat node
npx hardhat run --network localhost scripts/deploy.js
```
To deploy on a testnet:
```sh
npx hardhat run --network goerli scripts/deploy.js
```

## Testing
Run the test suite using Hardhat and Chai:
```sh
npx hardhat test
```

## Contract Details
### Smart Contract (`AITU_SE2315.sol`)
Located in `contracts/` directory, this contract implements an ERC20 token with the following functionalities:
- `getTransactionSender()`: Returns the address of the sender.
- `getBlockTimestamp()`: Returns the current block timestamp.
- `getTransactionReceiver(address _to)`: Returns the specified receiver address.
- `getLatestTransactionTimestamp()`: Converts and returns the latest transaction timestamp in a human-readable format.

### Unit Tests (`Aitu_SE2315-test.js`)
Located in `test/` directory, this script tests:
- Correct deployment and ownership assignment.
- Minting of initial supply.
- Retrieval of sender and receiver addresses.
- Conversion of timestamps into a human-readable format.

## Usage
Interact with the contract using Hardhat console:
```sh
npx hardhat console --network localhost
const contract = await ethers.getContractAt("AITU_SE2315", "DEPLOYED_CONTRACT_ADDRESS");
await contract.balanceOf("YOUR_ADDRESS");
```

## License
This project is licensed under the MIT License.

## Author
- **Yeskendir_Khasangaliev** - *Assignment3* 

