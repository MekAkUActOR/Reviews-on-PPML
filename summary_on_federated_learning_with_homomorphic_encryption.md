# Summary on Federated Learning with Homomorphic Encryption
## Existing technical directions
1. Common public key and private key, one central server for aggregation.
2. Different public keys and private keys for different clients (each private key will be devided to two fragments), one central server for adding noise, one authority for aggregation.
3. Common public key and private key (each client holds a fragment of the private key, and secret key and public key are generated collectively), one central server for aggregation and adding noise.
4. MK-HE such as xMK-CKKS

## Pros & Cons
- Pros: Simple scheme and easy to implement
- Cons: Weak threat model. Lower security guarantee because all clients share the private key (in reality it may not matter because despite the homomorphic encryption there must be another cryptosystem for communication.). Neglect the threaten from other clients.

- Pros: Different private keys and consider differential privacy
- Cons: Weak threat model. There are two extra trusted entities: the authority knows the intermediate model parameters with noise, and the central server knows the noise, and they can cooperate to hack. Neglect the threaten from other clients. Extremely huge overhead in the server side when there are lots of clients because of decryption and encryption.

- Pros: Very strong threat model. Agnostic secret key. No extra trusted entity. Consider differential privacy.
- Cons: Complex crypto system and hard to implement for federated learning. High overhead and latency.

## Promising direction
Not explored field: implementing (multiparty) homomorphic encryption on online federated learning, a real IoT federated learning senerio. Can target on NDSS, S&P, USENIX Sec, CCS, TDSC, TIFS, IoT

Can be an open=source benchmark or a tool with option for different security requirements.

And our task will be on IoT, so there must be a very large scale (hundreds of millions) number of client devices. So we should consider Federated Learning techs in large scale scenario (cross-device).

How about hirarchical Federated Learning with cross-device in lower level and cross-silo in the high level? In cross-device level we use MHE or even naive HE , and in cross-silo level we use xMK-CKKS, MHE, or BatchCrypt?
