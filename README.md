# beaconchain-validator

### Becoming a Validator
In order to become a Validator, you need to deposit exactly 32 ether into a smart contract on the proof-of-work main Ethereum blockchain (the one we have now). This generates something like a "validator membership card" which lets you participate in the new system. Validators will be responsible for a specific shard or two (to be added later), and one validator will be able to propose/attest for one to two shards. In other words, 1C of resources lets you validate on up to two shards. If you want to stake more ETH, you have to power up another 1C of resources. Staking pools thus become something of an impracticality, enhancing the network's decentralization.

You see, the goal is to have the two systems (PoW vs PoS) live side by side for a good while because - as we explained in the phases section above - the first two phases won't have any data transfer in the system at all, so we'll still be relying on the PoW chain to process our data transactions. The transition will be gradual and no, miners won't suddenly be out of a job or stuck with outdated hardware. In fact, things are looking up for them - that's something we'll discuss in the ProgPoW post a little later.

So, how long can I be a validator? And what was that all about with the slashing with Slasher and losing stake? And what are the validators validating if we don't have transactions right off the bat?

Slow down there, knowledge-thirsty reader! Let's tackle these one by one.

    1. A validator can remain in the system indefinitely, provided they don't misbehave.
    2. A validator will lose part of their stake (the 32 ether) periodically over time if they go offline. This loss will increase dramatically as time goes by which means shorter offline periods will be more forgiving than longer ones. The validator will not lose ALL of their stake - instead, the validator will keep losing until a certain threshold is reached (i.e. 28 ether) and then be kicked off the validators team. Several months will need to elapse before the validator can withdraw the remaining ether. The validator can also lose stake for misbehaving - claiming that a transaction is valid when it isn't. This punishment will be more severe, but it's not yet clear how severe. The loss of stake is called slashing (a part of your stake is slashed) and the algorithm doing this is called Slasher.
    3. The new blockchain will basically be empty or junk-filled blocks at first. Since there's no data and no shards to reference, the blocks on the beacon chain will not contain anything particularly useful.

A popular question is why burn the ether of misbehaving validators at all instead of distributing it to other validators in the network? The short answer is that burning ether gives value to everyone through distributed scarcity, whereas distributing it to remaining validators would encourage them to sabotage each other in an effort to get each other's slashed ether.
