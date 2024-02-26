# Haowen Liu (26-02-2024)

# Paper information
- Title: Multiparty Homomorphic Encryption from Ring-Learning-with-Errors
- Authors: Christian Mouchet, Juan Troncoso-Pastoriza, Jean-Philippe Bossuat and Jean-Pierre Hubaux
- Venue: PoPETs 2021
- Keywords: Multiparty Homomorphic Encryption

# Paper content
## Summary
Title: The paper is titled “Multiparty Homomorphic Encryption from Ring-Learning-with-Errors”. It proposes and evaluates a secure multiparty computation (MPC) solution based on multiparty homomorphic encryption (MHE).

Motivation: The paper aims to address the limitations of existing MPC solutions that rely on linear secret-sharing schemes (LSSS), such as high communication complexity, interactive circuit evaluation, and non-collusion assumptions. The paper argues that MHE-based MPC solutions have several advantages, such as public transcript, compact offline phase, and non-interactive circuit evaluation.

Contribution: The paper makes the following contributions:
- It introduces a novel multiparty version of the BFV homomorphic encryption scheme, which supports both additive and multiplicative homomorphic operations over a ring of polynomials3. It also presents novel protocols for relinearization, bootstrapping, and key switching in the multiparty setting.
- It instantiates the MHE scheme into a generic MPC protocol and shows that it can reduce the communication complexity from quadratic to linear in the number of parties, thus enabling secure computation among potentially thousands of parties and in various computing paradigms.
- It implements and evaluates the MHE scheme and the MPC protocol in the Lattigo open-source library and demonstrates its efficiency and scalability for three example circuits: private input selection, component-wise vector multiplication, and Beaver multiplication triples generation.

## Strengths
The paper is well-written, clear, and rigorous. It provides a comprehensive background and related work section, as well as detailed descriptions and security proofs of the proposed schemes and protocols. It also provides extensive experimental results and comparisons with state-of-the-art solutions, highlighting the practicality and applicability of the MHE-based MPC approach.

## Weaknesses
The paper has some limitations that could be addressed in future work, such as:
- The MHE-based MPC approach is restricted to arithmetic circuits over a ring of polynomials, which may not be expressive enough for some applications that require non-arithmetic functions or other plaintext domains.
- The MHE-based MPC protocol is only secure against passive adversaries, which may not be realistic in some scenarios where active attacks are possible. The paper does not discuss how to extend the protocol to active security or how to integrate zero-knowledge proofs for verifying the correctness of the computation.
- The MHE-based MPC protocol requires a large amount of public-key material and ciphertexts, which may incur significant storage and bandwidth costs. The paper does not explore how to optimize or compress the public keys and ciphertexts, or how to leverage techniques such as batching or packing to improve the performance.

- The MHE-based MPC approach works on arithmetic circuits over a ring of polynomials, which means that the parties can only perform addition and multiplication operations on polynomial coefficients. However, some applications may require more complex functions, such as bitwise operations, comparisons, logical operations, or hashing functions, which are not supported by the MHE scheme. Moreover, some applications may have different plaintext domains, such as binary strings, integers, or real numbers, which are not compatible with the polynomial representation. Therefore, the MHE-based MPC approach may not be expressive enough for some applications that require non-arithmetic functions or other plaintext domains.
Active attacks are malicious actions performed by an adversary who can deviate from the protocol, such as modifying, deleting, or injecting messages, or sending incorrect inputs or outputs. Active attacks can compromise the correctness, privacy, or fairness of the MPC protocol. For example, an active adversary can send a wrong ciphertext to influence the outcome of the computation, or reveal the secret inputs or outputs of other parties. The MHE-based MPC protocol is only secure against passive adversaries, who can only observe the messages exchanged by the parties, but cannot alter them or deviate from the protocol. The paper does not discuss how to extend the protocol to active security or how to integrate zero-knowledge proofs for verifying the correctness of the computation.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
(Can you do better?)

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)

The key generation step of the MHE scheme consists of two sub-steps: the ideal-secret-key generation and the collective encryption-key generation.
- The ideal-secret-key generation is a simple and non-interactive procedure, where each party independently samples a secret key share from a polynomial ring and adds them up to obtain the ideal secret key, which is never revealed in practice.
- The collective encryption-key generation is a multiparty protocol, where the parties use a common reference string to agree on a public polynomial and then use their secret key shares to compute a collective public key, which is used to encrypt their inputs.
- The collective encryption-key generation protocol ensures that the public key is semantically secure, meaning that it does not leak any information about the ideal secret key or the parties’ inputs. It also ensures that the public key is correct, meaning that it can be used to decrypt the encrypted outputs of the computation.
