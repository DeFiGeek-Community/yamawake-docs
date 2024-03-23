## Functions

## Function overview

#### Auction Organizers

The auction organiser can deploy auction contracts cheaply (\*2) on the Ethereum network in any auction format (\*1) and organise a token sale.

In addition to the information in the contract, meta-information such as the auction title, description and logo can be tied to the auction contract and stored off-chain to make it appealing to participants.

Once an auction is created, a separate page is created for each auction on Yamawake, allowing the auction organiser to perform operations such as collecting sales, while participants can bid and claim their allocated tokens from the individual auction page.

As a platform usage fee, the fee amount set for each auction format is collected from the total bid amount at the time of sales collection.

\*1) V1 only supports bulk auction formats. Template contracts defining auction formats will be added and updated by the community from time to time.

\*2) Each auction contract is deployed using the minimal proxy pattern, which is inexpensive to gas.  



#### Auction participants

Auction participants can perform operations such as bidding, requesting allocated tokens and refunding from individual auction pages.

