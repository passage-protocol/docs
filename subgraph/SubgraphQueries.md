# Sample Queries
## Samples of subgraph queries for Loyalty Ledgers or Passports

# V2 Passport

## Get Passport Membership
### Get all information regarding a passport NFT contract
```
{
passports(where: {id: "0x06b1d212b8da92b83af328de5eef4e211da02097"}) {
id
name
symbol
supply
baseUri royaltyWallet royaltyBasisPoints renderModule mintingModules beforeTransferModule
} }
```
```
{
"data": {
"passports": [ {
"id": "0x06b1d212b8da92b83af328de5eef4e211da02097", "name": "Test Passport",
"symbol": "TPP",
"supply": "20",
"baseUri": "https://api.passage.xyz/passport/metadata/", "royaltyWallet": "0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266", "royaltyBasisPoints": "0",
"renderModule": "0x00000000",
"mintingModules": [],
"beforeTransferModule": "0x00000000" }
] }
}
```

## Get Passport Membership's members 
### Get a list of members' wallet addresses of a specific membership NFT contract
```
 {
passports(where: {id: "0x06b1d212b8da92b83af328de5eef4e211da02097"}) {
members { member {
id
} }
} }
```
```
 {
"data": {
"passports": [ {
"members": [ {
"member": {
"id": "0x976ea74026e726554db657fa54763abd0c3a0aa9"
} },
{
"member": {
"id": "0x3c44cdddb6a900fa2b585dd299e03d12fa4293bc" }
}, {
"member": {
"id": "0x3c44cdddb6a900fa2b585dd299e03d12fa4293bc"
} },
{
"member": {
"id": "0x3c44cdddb6a900fa2b585dd299e03d12fa4293bc" }
}, {
"member": {
"id": "0x3c44cdddb6a900fa2b585dd299e03d12fa4293bc"
} }
] }
] }
}
```

## Get Passport Memberships of specific Member
### Get the list of Passport Membership NFT Contracts a specific member is enrolled in
```
 {
members(where: {id: "0x15d34aaf54267db7d7c367839aaf71a00a2c6a65"}) {
passports { passport {
id
} }
} }
```
```
 {
"data": {
"members": [ {
"passports": [ {
"passport": {
"id": "0x06b1d212b8da92b83af328de5eef4e211da02097"
} },
{
"passport": {
"id": "0x06b1d212b8da92b83af328de5eef4e211da02097" }
} ]
} ]
} }
```

## Get Membership Count
### Get the total count of unique wallet addresses per membership
```
 {
passports(where: {id: "0x06b1d212b8da92b83af328de5eef4e211da02097"}) {
memberCount
} }
```
```
  {
"data": {
"passports": [ {
"memberCount": "5" }
] }
}
```

## Get Member's Passport Roles
### Get a member's roles for passports
```
 Minter Role: 0x9f2df0fed2c77648de5860a4cc508cd0818c85b8b8a1ab4ceeef8d981c8956a6 Default Admin Role: 0x0000000000000000000000000000000000000000000000000000000000000000 Upgrader Role: 0x189ab7a9244df0848122154315af71fe140f3db0fe014031783b0946b8c9d2e3 Manager Role: 0x241ecf16d79d0f8dbfb92cbc07fe17840425976cf0667f022fe9877caa831b08
 ```
 ```
 {
member(id: "0x376424f7982acf2b9f5f0211fb331a954920e589") {
passportRoles { role {
id roleHash passport {
id
} }
} }
}
```
```
  {
"data": {
"member": { "passportRoles": [
{
"role": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091_0x00000000000000000000000000000 "roleHash": "0x0000000000000000000000000000000000000000000000000000000000000000", "passport": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091" }
} },
{
"role": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091_0x189ab7a9244df0848122154315af7 "roleHash": "0x189ab7a9244df0848122154315af71fe140f3db0fe014031783b0946b8c9d2e3", "passport": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091" }
} },
{
"role": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091_0x241ecf16d79d0f8dbfb92cbc07fe1 "roleHash": "0x241ecf16d79d0f8dbfb92cbc07fe17840425976cf0667f022fe9877caa831b08", "passport": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091" }
} },
{
"role": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091_0x9f2df0fed2c77648de5860a4cc508 "roleHash": "0x9f2df0fed2c77648de5860a4cc508cd0818c85b8b8a1ab4ceeef8d981c8956a6", "passport": {
"id": "0x709fa9b9e420150649bd502e97aff60fecb7d091" }
} }
] }
} }
```

# V2 Loyalty Ledger
## Get Loyalty Membership
### Get all information on a Loyalty Membership NFT contract, including tokens
```
  {
loyalties(where: {id: "0x1016b5aaa3270a65c315c664ecb238b6db270b64"}) {
renderModule beforeTransferModule implementation roles {
id
} tokens {
id
maxSupply
}
baseUri royaltyWallet royaltyBasisPoints
} }
```
```
  {
"data": {
"loyalties": [ {
"renderModule": "0x00000000", "beforeTransferModule": "0x00000000", "implementation": "0x00000000", "roles": [
{
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0x00000000000000000000000000000
}, {
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0x189ab7a9244df0848122154315af7 },
{
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0x241ecf16d79d0f8dbfb92cbc07fe1
}, {
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0x9f2df0fed2c77648de5860a4cc508 }
], "tokens": [
{
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0", "maxSupply": "0"
} ],
"baseUri": "https://api.passage.xyz/passport/metadata/", "royaltyWallet": "0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266", "royaltyBasisPoints": "0"
} ]
} }
```

## Get Loyalty Tokens owned by a specific member
### Get a specific member's Loyalty tokens(s) and their respective information
```
  {
members(where: {id: "0x15d34aaf54267db7d7c367839aaf71a00a2c6a65" }) {
loyaltyTokens { loyaltyToken {
id totalMinted maxSupply
} }
} }
```
```
 {
"data": {
"members": [ {
"loyaltyTokens": [ {
"loyaltyToken": {
"id": "0x1016b5aaa3270a65c315c664ecb238b6db270b64_0", "totalMinted": "303568491004841320000000", "maxSupply": "0",
"mintingModules": []
} },
{
"loyaltyToken": {
"id": "0xed179b78d5781f93eb169730d8ad1be7313123f4_0", "totalMinted": "207558592766583765999999", "maxSupply": "0",
"mintingModules": []
} }
] }
] }
}
```

## Get Loyalty Token for their owners
### Get unique list of wallet addresses under a specific Loyalty program
```
  {
loyalties(where: {id: "0x1016b5aaa3270a65c315c664ecb238b6db270b64"}) {
tokens {
tokenIdx
owners {
member(distinct_on: id) { id
} }
} }
}
```
```
  {
"data": {
"loyalties": [ {
"tokens": [ {
"tokenIdx": "0", "owners": [
{
"member": {
"id": "0x15d34aaf54267db7d7c367839aaf71a00a2c6a65" }
}, {
"member": {
"id": "0x3c44cdddb6a900fa2b585dd299e03d12fa4293bc"
} },
{
"member": {
"id": "0x90f79bf6eb2c4f870365e785982e1f101e93b906" }
}, {
"member": {
"id": "0x976ea74026e726554db657fa54763abd0c3a0aa9"
} },
{
"member": {
"id": "0x9965507d1a55bcc2695c58ba16fb37d819b0a4dc" }
} ]
} ]
} ]
} }
```

## Get Member's Loyalty Roles
### Get a member's roles for loyalty ledgers
```
  Minter Role: 0x9f2df0fed2c77648de5860a4cc508cd0818c85b8b8a1ab4ceeef8d981c8956a6 Default Admin Role: 0x0000000000000000000000000000000000000000000000000000000000000000 Upgrader Role: 0x189ab7a9244df0848122154315af71fe140f3db0fe014031783b0946b8c9d2e3 Manager Role: 0x241ecf16d79d0f8dbfb92cbc07fe17840425976cf0667f022fe9877caa831b08
```
```
 {
member(id: "0x376424f7982acf2b9f5f0211fb331a954920e589") {
loyaltyRoles { role {
id roleHash loyalty {
id
} }
} }
}
```
```
{
"data": {
"member": { "loyaltyRoles": [
{
"role": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604_0x00000000000000000000000000000 "roleHash": "0x0000000000000000000000000000000000000000000000000000000000000000", "loyalty": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604" }
} },
{
"role": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604_0x189ab7a9244df0848122154315af7 "roleHash": "0x189ab7a9244df0848122154315af71fe140f3db0fe014031783b0946b8c9d2e3", "loyalty": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604" }
} },
{
"role": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604_0x241ecf16d79d0f8dbfb92cbc07fe1 "roleHash": "0x241ecf16d79d0f8dbfb92cbc07fe17840425976cf0667f022fe9877caa831b08", "loyalty": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604" }
} },
{
"role": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604_0x9f2df0fed2c77648de5860a4cc508 "roleHash": "0x9f2df0fed2c77648de5860a4cc508cd0818c85b8b8a1ab4ceeef8d981c8956a6", "loyalty": {
"id": "0x75ccaa19961bac652f59a7f395d354827d735604" }
} }
] }
} }
```