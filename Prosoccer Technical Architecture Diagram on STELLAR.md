# Prosoccer Project Technical Documentation

## Overview

Prosoccer is the first multi-chain digital football platform that empowers soccer fans to own, trade, manage soccer teams and play in competitions.

## **Technical Architecture Diagram**

```mermaid
sequenceDiagram
    participant User
    participant Prosoccer Platform
    participant Multichain Blockchain
    participant Ethereum Blockchain
    participant Smart Contract

    User->>+Prosoccer Platform: Register and Create Account

    User->>+Prosoccer Platform: Purchase NFT (Players, coaches or team)
    Prosoccer Platform->>+Multichain Blockchain: Check blockchain network user is accessing from
    Prosoccer Platform->>+Ethereum Blockchain: Transaction Request (Purchase NFT)
    Ethereum Blockchain->>+Smart Contract: Execute NFT Purchase
    Smart Contract-->>-Ethereum Blockchain: NFT Purchase Executed
    Ethereum Blockchain-->>-Prosoccer Platform: Transaction Confirmation (NFT Purchased)
    Prosoccer Platform-->>User: NFT Ownership Confirmed

    User->>+Prosoccer Platform: Manage Football Team
    Prosoccer Platform-->>-User: Team management executed

    User->>+Prosoccer Platform: Enter Competition
    Prosoccer Platform-->>-User: Competition entry executed

    User->>+Prosoccer Platform: Receive Rewards
    Prosoccer Platform->>+Ethereum Blockchain: Transaction Request (Distribute Rewards)
    Ethereum Blockchain->>+Smart Contract: Execute Rewards Distribution
    Smart Contract-->>-Ethereum Blockchain: Rewards Distribution Executed
    Ethereum Blockchain-->>-Prosoccer Platform: Transaction Confirmation (Rewards Distributed)
    Prosoccer Platform-->>User: Rewards Credited
```

# Explanation

## User Registration and Wallet Creation

1. The user registers on the Prosoccer platform using their preferred chain (Ethereum blockchain)
2.

## Purchasing a Football Team NFT

1. The user purchases their digital assets (players, coaches or team) on the platform.
2. The platform check the chain the user is accessing from (Ethereum blockchain)
3. The platform sends a transaction request to the Ethereum blockchain.
4. The smart contract executes the NFT purchase.
5. The transaction is confirmed, and the platform notifies the user of their NFT ownership.

## Managing Football Team

1. The user manages their football team through the platform.
2. The platform execute the team management request.

## Entering Competitions

1. The user enters a competition.
2. The platform execute the competition entry request.

## Receiving Rewards

1. The user receives rewards for participating in competitions.
2. The platform sends a transaction request to the Ethereum blockchain.
3. The smart contract executes the rewards distribution.
4. The transaction is confirmed, and the platform notifies the user.
