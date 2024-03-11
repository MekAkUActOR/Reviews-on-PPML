# Haowen (22-02-2024)

# Paper information

- Title: Privacy-Preserving Federated Learning Using Homomorphic Encryption
- Authors: Jaehyoung Park, Hyuk Lim
- Venue: MDPI 2022
- Keywords: Homomorphic Encryption, Federated Learning, Key Management

# Paper content
## Summary
### Overview
The paper introduces a privacy-preserving federated learning (PPFL) algorithm leveraging homomorphic encryption (HE) to protect model parameters during aggregation in federated learning systems. This method allows the encryption of local model parameters without decryption, enhancing data security by employing different HE keys across nodes.

### Methodology
The methodology involves the utilization of HE for arithmetic operations on ciphertexts, enabling a centralized server to aggregate encrypted local model parameters. It introduces a distributed cryptosystem allowing for the use of different HE private keys within the same system.

### Results & Discussions
The paper presents a performance analysis and evaluation of the PPFL algorithm across various cloud computing-based federated learning service scenarios, demonstrating the effectiveness of the approach in enhancing privacy and security.

### Research Gap or Area of Improvement
Identifies the challenge of key management in federated learning systems and proposes a novel approach to address this issue by allowing different encryption keys for different nodes.

## Strengths
 The paper addresses an important problem of data privacy in federated learning scenarios, and presents a novel technique that allows each client to use a different HE key in the same system. The paper also provides a theoretical analysis of the security, computation, and communication costs of the proposed algorithm, and shows experimental results to verify its feasibility and effectiveness.

## Weaknesses
The paper assumes that the key generation center, the cloud server, and the computation provider are trusted and honest, which may not be realistic in some scenarios. The paper also does not compare the proposed algorithm with other existing privacy-preserving federated learning methods, such as differential privacy or secure multiparty computation. The paper also does not discuss the impact of the proposed algorithm on the learning accuracy and convergence rate of the federated learning model.


## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
The paper could be improved by relaxing some of the assumptions on the trustworthiness of the system entities, and by providing more security analysis and proofs. The paper could also benefit from comparing the proposed algorithm with other state-of-the-art methods in terms of privacy, efficiency, and accuracy. The paper could also explore the trade-offs between the key size, the data length, and the homomorphic operations in the proposed algorithm.

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)

This paper proposes a privacy-preserving federated learning algorithm that uses a distributed homomorphic cryptosystem to allow each client to use a different homomorphic encryption (HE) key in the same system1. Here is a brief explanation of how it works:
- Homomorphic encryption is a technique that allows arithmetic operations to be performed on encrypted data without decrypting them23. For example, if A and B are encrypted values, then HE can compute A + B or A * B without revealing the original values of A and B.
- Distributed homomorphic cryptosystem is a scheme that splits a private key into several partial private keys and distributes them to multiple servers4. This way, no single server can decrypt the encrypted data by itself, but they can cooperate to perform homomorphic operations and decryption.
- Privacy-preserving federated learning is a method that enables multiple clients to train a machine learning model collaboratively without sharing their local data5. Instead, they only share their local model parameters, which are encrypted with their own HE keys.

The paper’s algorithm works as follows:
- Each client generates its own public-private HE key pair and sends the public key to the central server and the computation provider. The private key is split into two partial private keys and distributed to the server and the provider.
- The server sends the global model parameters, encrypted with each client’s public key, to the clients6. The clients decrypt them with their private keys and train their local models with their local data7. Then, they encrypt their local model parameters with their public keys and send them back to the server.
- The server adds a random noise, encrypted with each client’s public key, to the encrypted local model parameters and partially decrypts them with its partial private key9. Then, it sends the partially decrypted values to the provider.
- The provider performs the final decryption with its partial private key and obtains the sum of the local model parameters and the random noise. Then, it calculates the average of the sum and encrypts it with each client’s public key. It sends the encrypted average to the server.
- The server removes the random noise from the encrypted average by using homomorphic subtraction and obtains the encrypted global model parameters8. It sends them to the clients for the next iteration.

By using this algorithm, the paper achieves the following advantages:
- Stronger privacy protection: Each client uses a different HE key, so even if one client’s key is compromised, the other clients’ data are still secure. Moreover, the server and the provider cannot access the clients’ data or model parameters without their cooperation.
- Higher flexibility: The clients can use different HE keys in the same system, so they do not need to agree on a common key or exchange keys with each other. This reduces the communication and coordination overhead.


According to part 3.3 of the current paper, the homomorphic encryption scheme used is the Paillier cryptosystem (PCK) [19]. This scheme is an additive homomorphic encryption (AHE) scheme that allows performing addition operations on ciphertexts without decryption12. The paper proposes a privacy-preserving federated learning (PPFL) algorithm that uses a distributed homomorphic cryptosystem (DHC) based on the PCK scheme to protect the local and global model parameters3. The paper also describes the functions and procedures of the DHC in detail.
