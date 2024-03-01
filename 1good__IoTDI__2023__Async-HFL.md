# Haowen (01-03-2024)

# Paper information
- Title: Async-HFL: Efficient and Robust Asynchronous Federated Learning in Hierarchical IoT Networks
- Authors: Yu, Xiaofan and Cherkasova, Lucy and Vardhan, Harsh and Zhao, Quanling and Ekaireb, Emily and Zhang, Xiyuan and Mazumdar, Arya and Rosing, Tajana
- Venue: ACM IoTDI
- Keywords: Asychronous Federated Learning, Hierarchical Federated Learning, Internet of Things

# Paper content
## Summary
The paper “Async-HFL: Efficient and Robust Asynchronous Federated Learning in Hierarchical IoT Networks” proposes a novel framework for federated learning (FL) in hierarchical Internet of Things (IoT) networks. The authors address several challenges specific to such networks, including data heterogeneity, system characteristics, unexpected stragglers, and scalability. Here are the key points from the paper:

#### Problem Statement and Motivation:
- The authors highlight the importance of FL in distributed IoT systems.
- They identify challenges related to data distribution, system heterogeneity, and stragglers in hierarchical networks.

#### Async-HFL Framework:
- The proposed framework employs asynchronous aggregation at both gateway and cloud levels.
- Device selection and device-gateway association modules are designed to optimize convergence under system heterogeneities.
- The approach balances learning utility, round latencies, and unexpected stragglers.

#### Simulation Results:
- Extensive simulations based on ns-3 and NYCMesh demonstrate that Async-HFL converges faster than state-of-the-art asynchronous FL algorithms.
- Communication cost savings are achieved without compromising convergence speed.

#### Physical Deployment Validation:
- The authors validate Async-HFL on a smaller physical deployment, observing robust convergence even under unexpected stragglers.

#### Contributions and Future Work:
- Async-HFL provides an end-to-end solution for hierarchical FL in IoT networks.
- Future work could focus on improving convergence speed for specific datasets (e.g., Shakespeare).

In summary, “Async-HFL” presents a promising approach to address FL challenges in hierarchical IoT networks. Its robustness, efficiency, and scalability make it a valuable contribution to the field.

## Strengths
#### Asynchronous Aggregation at Both Levels:
- Async-HFL employs asynchronous aggregation not only at the cloud level but also at the intermediate gateway level.
- This approach allows faster convergence by avoiding waiting times due to stragglers and heterogeneous delays.

#### Robustness to Stragglers:
- By incorporating intermediate gateway aggregation, Async-HFL ensures that even if some devices experience delays, the overall convergence remains robust.
- Stragglers can catch up after downloading the latest global model from the gateway.

#### Quantification of Data Heterogeneity:
Async-HFL introduces the concept of learning utility, which quantifies gradient diversity.
This metric helps balance the trade-off between statistical utility and system efficiency.

## Weaknesses
#### Complexity and Computational Overhead:
- The additional management modules (device selection and device-gateway association) increase the complexity of the framework.
- Solving Integer Linear Programs (ILPs) for these modules can be computationally expensive.

#### Dependency on Network Characteristics:
- Async-HFL’s performance heavily relies on the specific network topology, delays, and system characteristics.
- In real-world scenarios, these factors can vary significantly, affecting the framework’s effectiveness.

#### Scalability Challenges:
- While Async-HFL is designed for hierarchical networks, extending it to more complex architectures (e.g., multi-tiered or larger-scale hierarchies) may lead to performance degradation.
- Ensuring scalability while preserving gains remains an active research area.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
(Can you do better?)

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)
