# cnft-delist
An example to delist an NFT listed on the depreacated cardano marketplace

## First step: Remember your listing price

This is not really mandatory but, it helps a lot, if your listing price was 100 ADA, it will be 100000000 <--- This is the number we need

## Second step: Get the royalty address and % of the listed project

You can either get it from the 777 token or checking on jpg store, we need the public key hash of this address, to get it just go to https://cardanoscan.io/addressInspector and paste the royalty address, copy the Payment Credential field

## Third step: Get your publick key hash

We do the same thing but using the listing address, be 100% of what the listing address was

## Final step: Replace everything on the example file and run the code

  This is the most tricky part, go to https://cbor.me/ and paste this datum, replace the fields with your listing data and get the new datum to replace this one
  
  `d866820084581cfb2cd544a148d0bbc70c9863e3448224ee95c3db699f864f8d6305e2581c3342ca8c073a11b7664bd105123353e79c01116cc465915133fdcf75d8668200821b0000003a351a01c014d866820180`

  Example
  `102([0, [h'SELLER_SPENDING_KEY_HASH', h'ROYALTY_SPENDING_KEY_HASH', 102([0, [//LISTING_PRICE, //ROYALTY_PERCENTAGE_IN_MILLESIMALS]]), 102([1, []])]])`

  So something like this
  
  `102([0, [h'FB2CD544A148D0BBC70C9863E3448224EE95C3DB699F864F8D6305E2', h'3342CA8C073A11B7664BD105123353E79C01116CC465915133FDCF75', 102([0, [249999000000, 20]]), 102([1, []])]])`


Run the code on your browser and...

# Ta-Dà! Delisted.

