# NFT-Garage

https://krisht6.github.io/NFT-Garage/

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
