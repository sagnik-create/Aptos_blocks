# Auction Marketplace Module

## Overview
This module implements a decentralized auction marketplace on the Aptos blockchain. It allows users to list NFTs for auction, place bids, and claim NFTs or coins based on the auction outcome. 

## Features

- **Initialize Auction**: Set up the auction environment, including storage for auction data and locked coins.
- **Sell NFT**: List an NFT for auction with a set price and duration.
- **Bid**: Place bids on listed NFTs. The highest bid wins after the auction duration ends.
- **Claim Token**: Allows the highest bidder to claim the NFT once the auction ends.
- **Claim Coins**: Allows the seller to claim the funds once the NFT has been claimed by the bidder.

## Key Structures

1. **AuctionItem**: Holds details about each auction, including the seller, current bid, duration, and the locked NFT.
2. **AuctionData**: Stores all auction items and handles related events like bids and claims.
3. **CoinEscrow**: Manages the escrow of coins for ongoing bids.
4. **AuctionEvent**, **BidEvent**, **ClaimTokenEvent**: Events triggered during the auction lifecycle.

## Key Functions

- **initialize_auction**: Initializes auction data and coin escrow storage.
- **sell_nft**: Locks an NFT in the auction and lists it for sale.
- **bid**: Allows users to place a bid on an NFT.
- **claim_token**: Transfers the NFT to the highest bidder after the auction ends.
- **claim_coins**: Transfers the bid amount to the seller after the NFT is claimed.

## Tests

- **test_init**: Verifies the auction initialization process.
- **test_sell_nft**: Tests listing an NFT for auction.
- **test_bid_nft**: Tests placing a bid on an NFT.
- **test_claim_token**: Tests claiming the NFT by the highest bidder.
- **test_claim_coins**: Tests the seller's ability to claim the bid amount after the auction.

## Usage

1. **Initialize the Auction**: `initialize_auction`.
2. **List an NFT for Sale**: `sell_nft`.
3. **Place a Bid**: `bid`.
4. **Claim the NFT**: `claim_token`.
5. **Claim Coins**: `claim_coins`.