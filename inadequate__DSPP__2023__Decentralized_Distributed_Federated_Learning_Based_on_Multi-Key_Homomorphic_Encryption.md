# Haowen (29-02-2024)

# Paper information
- Title: Decentralized Distributed Federated Learning Based on Multi-Key Homomorphic Encryption
- Authors: Mengxue Shang; Dandan Zhang; Fengyin Li
- Venue: DSPP 2023
- Keywords: Hierarcical Federated Learning, xMK-CKKS

# Paper content
## Summary
This paper proposes a decentralized distributed federated learning scheme based on multi-key homomorphic encryption. The main contributions are:
- Decentralized framework: The paper introduces distributed servers (DS) to replace the central server in traditional federated learning, and uses consistent hash ring networking to achieve decentralized coordination of model training.
- Privacy-preserving mechanisms: The paper leverages xMK-CKKS to protect the clients’ data and model updates from honest-but-curious DS and external attackers, and uses CKKS to ensure the security of the DS’s local models during the global aggregation process.
- RingAllreduce algorithm: The paper adopts the RingAllreduce algorithm to perform efficient and robust communication and aggregation of local models among DS, without relying on a central server or proxy.

The paper provides security analysis and performance analysis to show the advantages of the proposed scheme over existing methods. The paper is well-written and organized, and the technical details are clear and rigorous. The paper also discusses some open challenges and future directions for the research field.

## Strengths
(Please evaluate the *work*, not the *presentation*)

## Weaknesses
Primarily the original xMK-CKKS but dividing the clients to several groups, so limited novelty. More communication rounds, hard to manage keys, and cannot tolerate unexpected stragglers and mobile devices in local federated learning phase because of xMK-CKKS.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
Instead of applying xMK-CKKS in local Federated Learning phase, using it in gateway aggregation is better, so every client device in a subdomain will share the same secret key.

Some possible suggestions for improvement are:
- Comparison with related work: The paper could provide more comparison and discussion with other related work on decentralized federated learning and multi-key homomorphic encryption, and highlight the novelty and significance of the proposed scheme.
- Experimental evaluation: The paper could provide some experimental results to demonstrate the effectiveness and efficiency of the proposed scheme in realistic scenarios, such as edge computing or IoT applications. The paper could also compare the performance of the proposed scheme with other state-of-the-art methods in terms of communication overhead, computation cost, and model accuracy.
- Scalability and robustness: The paper could address some potential issues and challenges regarding the scalability and robustness of the proposed scheme, such as how to handle the dynamic join and leave of clients and DS, how to deal with the heterogeneity and imbalance of data and computation resources among clients and DS, and how to cope with the malicious behavior or failure of clients and DS.

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)
