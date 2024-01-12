1.NFT identity verification:
NFT can be used for identity verification and auth as they can contain unique info about an individual that is cryptographyically secure.

thie contracts inherit from openzepplin erc 721 contract and adds identity verify function

_verified mapping keeps track of which addrs to verify 

verify functin / method allows the contract owner to verify an address while revoking the function. 
the checkVerifiedornot function allows any address to check if it has been verified by the contract owner.

the mint function allows the contract owner to mint new NFT's and assign them to verified address 
the "_beforeTokenTransfer" function is overridden to the identity verification check.
it makes sure that the senders and recievers token/address has been verified before allowing them the token transfer to proceed.