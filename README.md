
# 🚀 PumpFun APIs

PumpFun APIs empower developers to interact with Solana's bonding curve-based token operations with ease. Whether you're looking to buy or sell tokens, our API makes it seamless and efficient. Welcome to the future of Solana token transactions!

## 🌟 What is PumpFun API?

PumpFun API is your gateway to executing token trades on the Solana blockchain using bonding curve mechanisms. With customizable options like priority fees, slippage limits, and more, developers can integrate advanced trading features into their applications.

## 🌐 Base URL

All API requests should be made to the following base URL:

```
https://api.pumpfunapis.com
```

## 📋 API Endpoints

### 1. 🛒 Buy Tokens
**Endpoint:** `POST /api/buy`  
This endpoint lets you purchase tokens.

#### Full URL

```
https://api.pumpfunapis.com/api/buy
```

#### Request Payload

```json
{
  "private_key": "your_base58_private_key",
  "mint": "token_mint_address",
  "sol_in": 0.1,
  "slippage": 5,
  "priorityFee": 0.0001,
  "rpc": "https://custom.rpc.url" // Optional
}
```

- **private_key**: Your private key in Base58 format (required).
- **mint**: The mint address of the token you want to buy (required).
- **sol_in**: Amount of SOL to spend on the purchase (required).
- **slippage**: Allowed slippage percentage (required, 0-100).
- **priorityFee**: Custom priority fee in SOL (optional).
- **rpc**: Custom RPC endpoint URL (optional).

#### Response Example

```json
{
  "status": "success",
  "message": "Buy transaction confirmed.",
  "tx_signature": "5wVaP...riJa",
  "solscan_url": "https://solscan.io/tx/5wVaP...riJa"
}
```

### 2. 💰 Sell Tokens
**Endpoint:** `POST /api/sell`  
This endpoint lets you sell tokens with control over the percentage and slippage.

#### Full URL

```
https://api.pumpfunapis.com/api/sell
```

#### Request Payload

```json
{
  "private_key": "your_base58_private_key",
  "mint": "token_mint_address",
  "percentage": 50,
  "slippage": 10,
  "priorityFee": 0.0001,
  "rpc": "https://custom.rpc.url" // Optional
}
```

- **private_key**: Your private key in Base58 format (required).
- **mint**: The mint address of the token you want to sell (required).
- **percentage**: Percentage of your token balance to sell (required, 1-100).
- **slippage**: Allowed slippage percentage (required, 0-100).
- **priorityFee**: Custom priority fee in SOL (optional).
- **rpc**: Custom RPC endpoint URL (optional).

#### Response Example

```json
{
  "status": "success",
  "message": "Sell transaction confirmed.",
  "tx_signature": "8hTgM...ke7X",
  "solscan_url": "https://solscan.io/tx/8hTgM...ke7X"
}
```

## 📈 Why Use PumpFun API?

- **Ease of Use**: Simple endpoints to buy and sell tokens.
- **Customizable**: Specify priority fees and slippage for optimal transactions.
- **Solana Powered**: Built for speed and efficiency on Solana's blockchain.

## 🤝 Support

Need help? Contact our team or refer to our API documentation for additional guidance.

---

Optimize your Solana token trades today with PumpFun APIs! 🎉
