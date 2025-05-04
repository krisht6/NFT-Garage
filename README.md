# NFT-Garage

# Abstract
NFT Garage is a decentralized application (dApp), enabling users to mint, customize, and display digital cars NFTs on the Sepolia testnet. Using Ethereum smart contracts, the project automates the minting of five unique cars—Honda Civic, Subaru WRX, Lexus ES350, BMW M4 Competition, and Audi R8—stored as NFTs with metadata hosted on Pinata via IPFS. The front-end, hosted on GitHub Pages, integrates Web3.js for wallet interactions, allowing users to purchase NFTs using the Yoda ERC-20 token. Right now, the customization of car mods is done on the backend in Remix.

# Tech Stack
- Remix IDE (.sol file)
- VS Code (.html file)
- Github Local Host
- Github src Asset Management

# Key Features
**Decentralized Application (dApp):** Built on the Sepolia testnet, enabling users to interact with digital car NFTs.

**NFT Minting:** Automatically mints five unique car NFTs (Honda Civic, Subaru WRX, Lexus ES350, BMW M4 Competition, Audi R8) using Ethereum smart contracts.

**Customizable NFTs:** Allows owners to modify car attributes (paint, body kit, engine) via the updateCarMods function.

**Metadata Storage:** Car NFT metadata is hosted on Pinata via IPFS, ensuring decentralized and persistent storage.

**ERC-721 Compliance:** Inherits from OpenZeppelin's ERC721 for standard NFT functionality, with additional features like ownership and token URI management.

**Yoda ERC-20 Token Integration:** Uses the Yoda token for purchasing NFTs, facilitating transactions via the completeSale function.

**Front-End Interface:** Hosted on GitHub Pages, integrates Web3.js for seamless wallet interactions (e.g., MetaMask) to mint, buy, and customize NFTs.

**Backend Customization: **Car modifications are currently managed on the backend using Remix for smart contract interactions.

**Structured Car Data: **Stores car properties (model, paint, body kit, engine, performance score) in a Car struct, with performance score immutable after minting.

# Future Work
In the near future, NFT Garage aims to integrate the "garage" feature into the GUI, allowing users to modify car mods directly on the website, enhancing user experience. Additionally, plans include enabling users to mint custom car NFTs for a premium price and ensuring compatibility with OpenSea for seamless marketplace integration, while continuing to support MetaMask and crypto payments.

# Dependencies
Node.js and npm: Required for local development and building the front-end.

MetaMask: Browser extension for wallet interactions with the Sepolia testnet.

Remix IDE: For compiling, deploying, and interacting with the NFTGarage.sol smart contract.

Yoda ERC-20 Token: The token used for purchasing NFTs.

Web3.js: For front-end integration with Ethereum wallets.

GitHub Pages: For hosting the front-end.

Sepolia Testnet ETH: For gas fees during deployment and interactions.


# Minting an NFT in Remix

The NFTGarage.sol contract pre-mints five car NFTs during deployment. To modify one of these NFTs (e.g., change paint, body kit, or engine), follow these steps:

**Open Remix:**
Go to https://remix.ethereum.org.
Upload or paste NFTGarage.sol into the Remix File Explorer.

**Compile the Contract:**
Select the Solidity compiler (version ^0.8.20).
Click "Compile NFTGarage.sol".

**Deploy the Contract:**
In the "Deploy & Run Transactions" tab, select "Injected Provider - MetaMask" as the environment.
Connect MetaMask to the Sepolia testnet and ensure you have testnet ETH.
Enter the Yoda ERC-20 token contract address in the constructor field (e.g., 0xYourYodaTokenAddress).
Click "Deploy" and confirm the transaction in MetaMask.

**Mint and Modify an NFT:**
The contract automatically mints five car NFTs (token IDs 1–5) to the deployer’s address during deployment.
To modify an NFT (e.g., token ID 1), call the updateCarMods function:
Select the deployed contract in Remix.
Enter the tokenId (e.g., 1).
Provide new values for newPaint (e.g., "Candy Red"), newBodyKit (e.g., "Carbon Fiber"), newEngine (e.g., "2.0L Turbo"), and newTokenURI (e.g., a new IPFS URI from Pinata, like ipfs://bafkrei...).
Click "transact" and confirm in MetaMask.
Verify the updated attributes by calling the cars mapping with the tokenId.


# Minting a Car NFT via the GUI

The GUI allows users to purchase one of the five pre-minted car NFTs using Yoda tokens. Note: Custom minting is not yet supported in the GUI.

**Access the UI:**
Open the deployed GitHub Pages site (https://krisht6.github.io/NFT-Garage/) or run locally (npm start).

**Connect MetaMask:**
Click the "Connect Wallet" button in the UI.
Ensure MetaMask is set to the Sepolia testnet and has Yoda tokens and testnet ETH.

**Purchase an NFT:**
Browse the available car NFTs (Honda Civic, Subaru WRX, etc.) displayed in the UI.
Select a car (e.g., token ID 1) and click "Buy".
Approve the Yoda token transfer and confirm the completeSale transaction in MetaMask.
The NFT will transfer to your wallet, viewable in MetaMask or compatible platforms like OpenSea (Sepolia testnet).

**Verify Ownership:**
Check your wallet in MetaMask or query the contract’s ownerOf function with the tokenId in Remix to confirm ownership.


