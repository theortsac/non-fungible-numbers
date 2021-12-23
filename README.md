## Non-Fungible Numbers 🔢
The "Non-Fungible Numbers" project lets you own a specific number forever on the Polygon blockchain! It was made in one day by me, after just starting the [CryptoZombies](https://cryptozombies.io/) course. I really liked how it turned out, but it isn't supposed to make money! Each mint costs 0.0000001 MATIC, which means I would need 3.5 million numbers minted to get to $1 worth of MATIC on the contract's balance.
To use the smart contract deployed on the Polygon blockchain, just access [this link](https://polygonscan.com/address/0x96faabece7f7c6421c9a104f2d0cb2611466e584) and click `Contract` (the one with the checkmark). Then you can click read and write contract to start interacting with it! Here is a simple guide if you want to mint your own number:
- Access [this link](https://polygonscan.com/address/0x96faabece7f7c6421c9a104f2d0cb2611466e584).
- Click on `Contract ✓`.
- Click on `Read Contract`.
- Click on `isNumberMinted` and put the number you want to mint, then click query, if the result is false you can proceed. If it's true you will need to try another number.
- Click on `Write Contract`.
- Click on `mint`.
- Put the number from the step before before before this one on `_number (uint256)`.
- Put `0.0000001` on `mint` (the field just above `_number (uint256)`).
- Connect your wallet.
- Click `Write`.
- Approve the transaction on metamask.
- You are done, congrats!
- Extra Tip: Go to the [MATIC faucet](https://matic.supply/) and get your free 0.0005 MATIC, which is enough to cover the 0.0000001 mint price. If gas is a high and it can't cover it you can use the faucet up to 3 times a day, so just use it whenever you can and really soon (same day) you will get enough for your own number!

|          Name          | Privacy |  Type |                                        Action                                        | OwnerOnly |
|:----------------------:|:-------:|:-----:|:------------------------------------------------------------------------------------:|:---------:|
|          mint          |  public | write |                 mint the chosen number if<br>it wasn't minted already                |     ❌     |
| _removeNumberFromOwner | private | write |                remove the selected number<br>from the selected address               |     ❌     |
|     transferNumber     |  public | write |    transfer a number from the<br>address that wants to transfer<br>to another one    |     ❌     |
|    transferOwnership   |  public | write | transfer the ownership of the<br>contract (allows withdraw) to<br>a selected address |     ✅     |
|        withdraw        |  public | write |             send all the balance of the<br>contract to the current owner             |     ✅     |
|   addressOwnsNumbers   |  public |  view |                   check which numbers the selected<br>address owns                   |     ❌     |
|   howManyNumbersOwned  |  public |  view |                  check how many numbers the<br>selected address owns                 |     ❌     |
|     isNumberMinted     |  public |  view |                        check if a specific number is<br>minted                       |     ❌     |
|      numberOwnedBy     |  public |  view |                    check who is the owner of a<br>specific number                    |     ❌     |
|       totalSupply      |  public |  view |                     check how many numbers were<br>minted so far                     |     ❌     |
