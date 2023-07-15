
# Project Title

A non-fungible token (NFT) marketplace project is a platform that enables the buying, selling, and trading of NFTs. NFTs are unique digital assets that are stored on a blockchain, typically on Ethereum or another blockchain that supports smart contracts. Unlike cryptocurrencies such as Bitcoin or Ethereum, which are fungible and can be exchanged on a one-to-one basis, NFTs are indivisible and have distinct properties that make them unique and irreplaceable.

An NFT marketplace serves as an online marketplace where creators and collectors can interact and transact with NFTs


## Environment Variables

To run this project, you will need to add the following environment variables to your .env.local file

`NEXT_PUBLIC_PROJECT_ID`

`NEXT_PUBLIC_PROJECT_SECRET`

These variables are required for storing the images on the IPFS provided services.
You can get the mentioned `ID` and `SECRET` from their website after creating an account.
## Run Locally

Clone the project

```bash
  git clone https://github.com/Notoriousbrain/nft-marketplace.git
```

Go to the project directory

```bash
  cd nft-marketplace
```

Install dependencies

```bash
  npm install
```

YOU WILL REQUIRE 3 PARALLEL RUNNING SERVERS FOR THE LOCAL SETUP

Start Server 1

```bash
  npx hardhat node
```

Start Server 2

```bash
  npx hardhat run scripts/deploy.js --network localhost
```

In case you encounter an error in server 2 such as ```Unidentified flag --network localhost``` then run the 2nd server without the flag

```bash
  npx hardhat run scripts/deploy.js
```

Start Server 3

```bash
  npm run dev
```
## MetaMask
In your MetaMask account: go to settings > network > add network

Add a new network

```
  Network Name = HardhatNetwork || 'any name you want'
  New RPC URL = http://127.0.0.1:8545/
  Chain ID = 1337
  Currency Symbol = ETH
```

After creating the new network select the network, from the available networks, as the active network

#### Add a new account by selecting on the accounts dropdown
After opening the accounts dropdown, click on `Import account`

In the first server, you will be provided with 20 demo accounts, copy any of the demo accounts `private key` and click on import. 

Now you have a demo account with 10000 demo ETH <Not original ETH> to use.
## Features

- Light/dark mode toggle
- Live previews
- Searching for existing tokens from the marketplace
- Creating new tokens for the market place

