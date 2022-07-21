# Full-Stack Setup

## 1. Git clone the contracts repo

In it's own terminal / command line, run: 

```
git clone https://github.com/Nedick/hardhat-nft-marketplace
cd hardhat-nft-marketplace
yarn
```

## 2. Deploy to NftMarketplace on rinkeby

After installing dependencies, start a node on it's own terminal with:

```
yarn hardhat deploy --network rinkeby
```

## 3. Deploy the subgraph

```
cd ..
https://github.com/Nedick/thegraph-nft-marketplace.git
cd thegraph-nft-marketplace
yarn
```

Follow the instructions of the [README](https://github.com/Nedick/thegraph-nft-marketplace/blob/main/README.md) of that repo. 

Then, make a `.env` file and place your temporary query URL into it as `NEXT_PUBLIC_SUBGRAPH_URL`.

## 4. Start your UI

Make sure that:
- In your `networkMapping.json` you have an entry for `NftMarketplace` on the rinkeby network. 
- You have a `NEXT_PUBLIC_SUBGRAPH_URL` in your `.env` file. 

```
yarn dev
```
