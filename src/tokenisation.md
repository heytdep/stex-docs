# Document Tokenisation
Document tokenisation is very important is sTeX, but what exactly is happening as we tokenise a document we have written? This is a high-level description of how that works.

#### 1. Auth verificaton
This is a step that takes place in all of the described API endpoints, were the backend verifies the validity of the provided auth token.

#### 2. Building the transaction
Tokenisation happens as soon as we submit transaction to the Stellar network with the following operations:
- creating the document on chain (remember that the document keypair already exists)
- add the specified holder as the only signer of the document (this makes sure everything after the tokenisation is completely decentralised and non custodial)
- adding the hash of the contents to the document account as data attribute.
This transaction also has some sponsoring ops to make the process smoother which we are not specifiying for simplicity.

#### 4. Tokenise: sending the transaction
This process, which is completed client-side so the user can confirm the transaction, consists of simply sending the transaction to the network.

### Tokenise a document
```
POST /stellar/bridge/detach

Auth: YOUR_AUTH_TOKEN

{
    "id": DOCUMENT_ID,
    "holder": HOLDER_PUBLIC_KEY
}
```
