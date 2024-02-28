# Haowen (27-02-2024)

# Paper information

- Title: Privacy-preserving federated learning based on multi-key homomorphic encryption
- Authors: Jing Ma, Si-Ahmed Naas, Stephan Sigg, Xixiang Lyu
- Venue: Int J Intell Syst 2022
- Keywords: xMK-CKKS, Federated Learning, Privacy-Preserving Technology

# Paper content
## Summary
This paper proposes a novel scheme for privacy-preserving federated learning based on multi-key homomorphic encryption (MK-HE). The authors improve the existing MK-HE scheme, MK-CKKS, to design xMK-CKKS, which simplifies the decryption process and enhances the security against collusion attacks. Based on xMK-CKKS, the authors develop a federated learning scheme that allows distributed devices to collaboratively train a machine learning model without revealing their local data or model updates. The authors evaluate their scheme in terms of communication and computation cost, energy consumption, and model accuracy, and compare it with other state-of-the-art schemes based on homomorphic encryption.

The paper is well-written and organized, and the proposed scheme is novel and interesting. The authors provide sufficient background and motivation for their work, and explain the main ideas and techniques clearly. The paper also presents a detailed security and functionality analysis, and demonstrates the effectiveness and efficiency of the scheme through experiments on realistic IoT devices.

## Strengths
The paper makes the following contributions:

- It introduces xMK-CKKS, an improved version of MK-CKKS, which avoids the risk of data leakage and the need for an additional interactive protocol in the collaborative decryption process of MK-CKKS. xMK-CKKS is suitable for federated learning and other distributed scenarios.
- It establishes a privacy-preserving federated learning scheme based on xMK-CKKS, which achieves secure and efficient sum aggregation of all participants’ model updates. The scheme is resistant to attacks from internal curious participants as well as external malicious adversaries, and can withstand collusion between k < N − 1 compromised participating devices and the server.
- It evaluates and compares the scheme with other homomorphic encryption-based federated learning schemes in a realistic federated learning scenario using Jetson Nano IoT devices. The results show that the scheme outperforms other schemes in communication and computation cost while preserving model accuracy.

## Weaknesses
The paper also has some limitations and possible directions for future work:

- The paper assumes that all devices participate in each aggregation round, which may not be realistic in some scenarios where devices have limited availability or connectivity. It would be interesting to extend the scheme to handle dynamic and asynchronous participation of devices.
- The paper focuses on the additive homomorphism of xMK-CKKS, which is sufficient for federated averaging. However, some federated learning tasks may require more complex operations, such as multiplication or convolution. It would be useful to explore how to support these operations efficiently and securely using xMK-CKKS or other MK-HE schemes.
- The paper does not consider the impact of noise or quantization on the model accuracy and convergence. Since xMK-CKKS is an approximate fixed-point arithmetic scheme, it may introduce some errors or distortions in the encryption and decryption process. It would be important to analyze how these errors affect the learning performance and how to mitigate them.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
(Can you do better?)

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)
