# TemplateV1 (Fair Auction)

IBAO (Initial Bulk Auction Offering) Template

### Overview.

This is an auction format in which all bidders split a certain amount of ERC20 tokens offered by the organiser.

Participants (bidders) can bid in ETH and get a percentage of tokens equal to their individual bid percentage of the total bid amount.

As everyone gets tokens at the same price, there is no advantage or disadvantage depending on the timing of the bids.

The amount of the allocated amount will not be known until the final total bid is determined.

The higher the bid amount, the higher the price of the tokens (lower the quota) and the lower the price (higher the quota).





### Template fixed parameters

#### Minimum bid amount

0.001 ETH

#### Platform usage fee

1% of the total bid amount (deducted from the total bid amount upon sales collection)

#### Initial user reward factor

100





### Parameters required for holding

#### Token address

The address of the ERC20 token you wish to sell.

#### Duration of the event

You can specify a period of up to 30 days.

#### Allocation quantity

The quantity of ERC20 tokens you wish to sell.

#### Minimum amount raised

The minimum total bid that considers the auction a success. If not reached, the sale will be cancelled, the auction organiser will collect the tokens and the participants will collect their bids.

#### Other auction information

Information about the auction, including a project overview. It is tied to the auction contract and stored off-chain.

###

### Technical specifications

Detailed technical specifications can be found at.

[https://github.com/DeFiGeek-Community/yamawake/blob/main/doc/ja/Template/V1/index.md] (https://github.com/DeFiGeek-Community/ yamawake/blob/main/doc/en/Template/V1/index.md )

###

### Auction flow.

✅ **Before the auction**.

&#x20; Auction organiser launches auction

✅ **During the auction**.

&#x20; Auctioneers place bids

✅ **After the auction**.

* Upon a successful auction.

  * Auction organiser collects bid tokens

    * Initial user reward score for the auction organiser is credited

    * Within 3 days after the end of the auction.

      * Calculate allocated amount against minimum bid (0.001 ETH) and standby if 0

  * Auction participant claims sales tokens

    * If the allocation of auction tokens is more than 1 minimum unit.

      * Add the initial user reward score for the auction participant

      * Auction participant claims an allocated amount of tokens

    * If the auction token quota is zero

      * Recover the bid amount if the auction organiser has not yet collected the bid token

* If the auction fails.

  * Auction organiser recovers the sale tokens

  * Auctioneer recovers bid tokens

