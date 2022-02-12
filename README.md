# club721-ali-whitelist-raffle
[ALI](https://www.alinft.io/home) whitelist raffle for club721 membership holders.

## contract
A [contract](https://polygonscan.com/address/0xdc9b0af748272e154cd4cde7752222328fc1453f) used for this raffle

## raffle outcome
raffle [event](https://polygonscan.com/tx/0x1fdef80d71e16220b2cb8b87496e5b3ca66d496b7ecb6e99b69ba08405eb26ee#eventlog)

```
FinishRaffle (bytes32 requestId, bytes32 merkleRoot, uint256 randomSeed)

requestId : EFCEAF219A003A200D4EAD89A4B13FBB2D5ACA448920570738613E0B114AD03D
merkleRoot : B52973868C09627040A559FC6A785817CAEA05C11672383C8836CF5BFBB54C05
randomSeed : 528968754230860986568911771310116897763848326158270639638195258992774
```

| amount | weight | probability            |
|--------|--------|------------------------|
| 237    | 10     | 0.0021168501270110076  |
| 52     | 11     | 0.0023285351397121083  |
| 1      | 80     | 0.01693480101608806    |
| 1      | 40     | 0.00846740050804403    |
| 3      | 12     | 0.002540220152413209   |
| 2      | 14     | 0.0029635901778154107  |
| 1      | 15     | 0.0031752751905165114  |
| 1352   | 1      | 0.00021168501270110075 |
| 93     | 2      | 0.0004233700254022015  |
| 7      | 3      | 0.0006350550381033022  |
| 1      | 7      | 0.0014817950889077054  |
| 1      | 4      | 0.000846740050804403   |
| 1      | 5      | 0.0010584250635055038  |
| 1      | 8      | 0.001693480101608806   |

## Instruction to verify your entry
1. Go to [the contract on polygonscan](https://polygonscan.com/address/0xdc9b0af748272e154cd4cde7752222328fc1453f#readContract) and locate method `6. verifyProof`
2. Find you merkle proof in [data/proofs.json](./data/proofs.json)
3. Copy & Paste `idx`, `proof`, `weight` into the the boxes. And also your address into the `account`.
4. Put `B52973868C09627040A559FC6A785817CAEA05C11672383C8836CF5BFBB54C05` merkle root into the `merkleRoot (bytes32)`
5. Click `Query`. If you see `true`, you successfully enter the raffle.

## Instruction to get winners from contract
1. Go to [the contract on polygonscan](https://polygonscan.com/address/0xdc9b0af748272e154cd4cde7752222328fc1453f#readContract) and locate method `4. getWinners`
2. Put `B52973868C09627040A559FC6A785817CAEA05C11672383C8836CF5BFBB54C05` merkle root into the `merkleRoot (bytes32)`
3. Put `1000` into `n` and `0` into `skip`
4. Click `Query`. First 100 unique numbers are the winners' `idx` in the [data/proof](./data/proofs.json)
