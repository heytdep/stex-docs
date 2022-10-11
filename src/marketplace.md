# The sTeX decentralised marketplace
A more detailed specification of the marketplace and the degree of decentralisation it offers is currently being written, but below is how the invokation for basic trading of documents through the marketplace looks like.

### Make a sell offer for a document

Invoke the contract with the following body:

```json
{
    "timebounds":{"minTime":TIME_STAMP,"maxTime":TIME_STAMP},
    "fee":FEE,
    "action":"sellOffer",
    "sellerPK": SELLER_PUBLIC_KEY,
    "price": DOCUMENT_PRICE,
    "documentPK": DOCUMENT_ID
}
```

### Make a buy offer for a document

Invoke the contract with the following body:

```json
{
    "timebounds":{"minTime":TIME_STAMP,"maxTime":TIME_STAMP},
    "fee":FEE,
    "action":"buyOffer",
    "buyerPK": SELLER_PUBLIC_KEY,
    "documentPK": DOCUMENT_ID
}
```
