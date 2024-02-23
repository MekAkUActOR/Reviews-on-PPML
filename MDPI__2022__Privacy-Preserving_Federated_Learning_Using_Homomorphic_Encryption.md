# Your name (Date)

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


Totally unfeasible and inscalable.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
The paper could be improved by relaxing some of the assumptions on the trustworthiness of the system entities, and by providing more security analysis and proofs. The paper could also benefit from comparing the proposed algorithm with other state-of-the-art methods in terms of privacy, efficiency, and accuracy. The paper could also explore the trade-offs between the key size, the data length, and the homomorphic operations in the proposed algorithm.

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)
