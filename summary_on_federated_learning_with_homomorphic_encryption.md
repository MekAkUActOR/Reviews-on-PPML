# Summary on Federated Learning with Homomorphic Encryption
## Existing technical directions
1. Common public key and private key, one central server for aggregation.
2. Different public keys and private keys for different clients (each private key will be devided to two fragments), one central server for adding noise, one authority for aggregation.
3. Common public key and private key (each client holds a fragment of the private key, and secret key and public key are generated collectively), one central server for aggregation and adding noise.

## Pros & Cons
- Pros: Simple scheme and easy to implement
- Cons: Weak threat model. Lower security guarantee because all clients share the private key (in reality it may not matter because despite the homomorphic encryption there must be another cryptosystem for communication.). Neglect the threaten from other clients.

- Pros: Different private keys and consider differential privacy
- Cons: Weak threat model. There are two extra trusted entities: the authority knows the intermediate model parameters with noise, and the central server knows the noise, and they can cooperate to hack. May have high overhead. Neglect the threaten from other clients.

- Pros: Very strong threat model. Agnostic secret key. No extra trusted entity. Consider differential privacy.
- Cons: Complex crypto system and hard to implement for federated learning. High overhead and latency.

## Promising direction
Not explored field: implementing (multiparty) homomorphic encryption on online federated learning, a real IoT federated learning senerio. Can target on NDSS, S&P, USENIX Sec, CCS, TDSC, TIFS, IoT

Can be an open=source benchmark or a tool with option for different security requirements.
