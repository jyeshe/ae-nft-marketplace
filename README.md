# AE NFT Marketplace
This is proof-of-concept P2P NFT Marketplace. 

It benefits from being decentralized and therefore highly available, auditable and with predictable rules and costs.

It's made out of fun allowing buyers to bargain over a reference price published by the seller.

An auction is created by the owner of the NFT using the `put_listing` entrypoint and bids are put in through `put_offer` requiring a transaction value to be locked. In case the offer is not accepted, a bid might be cancelled with `withdraw_offer` and the seller might give up the auction by `cancel_listing`. 

A trade is concluded when a seller accepts the highest bid with `accept_offer`.

For every change on an auction state, an event is emitted allowing the [ae_mdw](https://github.com/aeternity/ae_mdw) to track all operations.




