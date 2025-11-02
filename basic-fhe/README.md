# Basic FHE Operations Example

Learn the fundamentals of Fully Homomorphic Encryption with ZKEncrypt SDK.

## What You'll Learn

- Initialize ZKEncrypt SDK
- Encrypt and decrypt data
- Perform homomorphic addition
- Perform homomorphic multiplication
- Work with encrypted types

## Installation

```bash
npm install
```

## Usage

```bash
npm start
```

## Code Example

```typescript
import { ZKEncryptSDK } from '@zkencrypt/sdk';

// Initialize SDK
const sdk = new ZKEncryptSDK({
  network: 'devnet',
  rpcUrl: 'https://api.devnet.solana.com',
});

// Encrypt data
const publicKey = 'YOUR_PUBLIC_KEY';
const encrypted = await sdk.encrypt({
  data: 'Sensitive information',
  publicKey,
});

console.log('Encrypted:', encrypted.ciphertext);

// Decrypt data
const privateKey = 'YOUR_PRIVATE_KEY';
const decrypted = await sdk.decrypt({
  ciphertext: encrypted.ciphertext,
  privateKey,
});

console.log('Decrypted:', decrypted.data);

// Homomorphic addition
const value1 = await sdk.fhe.encrypt('10', publicKey);
const value2 = await sdk.fhe.encrypt('20', publicKey);
const sum = await sdk.fhe.add(value1.ciphertext, value2.ciphertext, publicKey);

console.log('Encrypted sum:', sum);
```

## Next Steps

- Try [Confidential Token Example](../confidential-token)
- Read [FHE Concepts](../tutorials/fhe-concepts.md)
- Explore [Private Auction](../private-auction)
