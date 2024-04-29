# Property App Smart Contract

This repository contains the smart contract implementation for the Property App, a decentralized application (DApp) designed for managing property transactions. The smart contract is written in PyTeal, the Python binding for writing Algorand smart contracts.

## Description

The smart contract facilitates various operations related to property transactions, including creation, management, and updating of property listings. It ensures the integrity and security of transactions while leveraging the Algorand blockchain's features for transparency and decentralization.

## Implementation Details

- **Smart Contract Language**: PyTeal
- **Blockchain Platform**: Algorand
- **Deployment Method**: On-chain deployment
- **Testing Environment**: Algorand TestNet

## Usage

To deploy the smart contract and initialize the Property App:

1. Ensure you have your unique MNEMONIC key ready.
2. Use your unique address on the Algorand TestNet to add funds to your account.
3. Deploy the smart contract to the Algorand TestNet using the Algorand SDK or any compatible tool.
4. Confirm the deployment by interacting with the deployed smart contract using your wallet or any Algorand-compatible client.

## Important Information
MNEMONIC KEY can be located in the Config file in the property Backend repository.
Transaction ID if needed will be available on request. 



## Repository Structure

- `/contracts`: Contains the PyTeal smart contract files.
- `/scripts`: Utility scripts for deployment and interaction with the smart contract and test of logic.


## Further Instructions
The instructions below contain pre steps taken to develop the smart contract.




# Algorand Song Vote Tutorial

The present tutorial is designed to cater to the needs of programmers with varying degrees of proficiency, who aspire to engage in web3 development or Algorand chain development. A basic comprehension of javascript, python, and smart contracts would suffice as a prerequisite to engage with the content. The tutorial is structured in a manner that facilitates progressive learning, with the aim of enabling the participant to attain a comprehensive understanding of the Algorand development pipeline and successfully create a functional dapp.



## Usage

- Install the dependencies.
```bash
cd algorand-backend
npm install
```

- Create the python virtual environment and install the dependencies.
```bash
python3 -m venv venv
. venv/bin/activate
pip install -r requirements.txt
```

- Run the first file to create an account.
```bash
node scripts/1-create-account.js
```
Make sure you saved the account data and open in in a wallet created on [Pera Wallet](https://web.perawallet.app/)

- Run the songvote script in python to create the artifacts

```bash
python3 contracts/songvote.py
```

- Deploy the smart contracts
Make sure you changed the mnemonic in:
```javascript
let myaccount = algosdk.mnemonicToSecretKey("your mnemonic");
```
Then run the script.
```bash
node scripts/5-deploy-songvote.js
```

- Start the front-end
```bash
cd ..
cd songvote
```

Make sure you update the app id with the one from the terminal earlier
```javascript
  // CHANGE THIS TO YOUR APP ID
  const app_address = YOUR APP ID;
  // CHANGE THIS TO YOUR APP ID
```
When the code is prepared, install the dependencies:
```bash
npm install
```

Then start the dev server:
```bash
npm run dev
```






## Acknowledgements

 - [Antony Silvetti-Schmitt for the origial tutorial](https://github.com/Antony-SS?tab=repositories)
 - [Vite Templates](https://vitejs.dev/)
