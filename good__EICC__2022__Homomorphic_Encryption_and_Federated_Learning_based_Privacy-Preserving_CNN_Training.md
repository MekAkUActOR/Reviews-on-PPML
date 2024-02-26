# Haowen (23-02-2024)

# Paper information
- Title: Homomorphic Encryption and Federated Learning based Privacy-Preserving CNN Training: COVID-19 Detection Use-Case
- Authors: F Wibawa, FO Catak, M Kuzlu, S Sarp, U Cali
- Venue: EICC 2022
- Keywords: Homomorphic Encryption, Federated Learning, COVID-19 Detection

# Paper content
## Summary
Overview: The paper proposes a privacy-preserving federated learning algorithm based on convolutional neural networks (CNNs) and homomorphic encryption (HE) for COVID-19 detection using X-ray scans. The paper uses a secure multi-party computation protocol to protect the model weights from adversaries during the aggregation phase. The paper evaluates the proposed algorithm using a real-world medical dataset and shows that it can achieve similar prediction performance as the plain-domain method.

## Strengths
Strengths: The paper addresses an important and timely problem of privacy and security of medical data in federated learning settings. The paper provides a clear and detailed description of the proposed algorithm and the underlying cryptographic scheme (BFV). The paper also presents experimental results to demonstrate the feasibility and effectiveness of the proposed algorithm in terms of prediction performance and execution time.

## Weaknesses
Weaknesses: The paper lacks a thorough analysis of the security and privacy guarantees of the proposed algorithm. The paper does not discuss the potential attacks or threats that the algorithm may face, nor the assumptions or limitations of the BFV scheme. The paper also does not compare the proposed algorithm with other existing methods or baselines for privacy-preserving federated learning. The paper could benefit from more discussion on the trade-offs between security, privacy, performance, and efficiency in the proposed algorithm.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
Suggestions: The paper could improve by providing more security and privacy analysis of the proposed algorithm, such as the level of security, the noise budget, the ciphertext expansion, and the privacy leakage. The paper could also include more related work and comparisons with other methods for privacy-preserving federated learning, such as differential privacy, secure aggregation, or multi-key HE. The paper could also explore other applications or datasets for the proposed algorithm, such as CT scans or MRI images.

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)
