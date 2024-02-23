# Haowen (21-02-2024)

# Paper information
(Please use comma as a separator for authors)
(For the venue use the abbreviated conference/journal name: e.g., MICRO 2019)
(Use as many keywords as you wish and don't make them too general)

- Title: Learning Without Knowing: Applying Homomorphic Encryption to Machine Learning Algorithms
- Authors: Yao
- Venue: Thesis
- Keywords: Homomorphic Encryption, Machine Learning, Security Proof

# Paper content
## Summary
### Overview
This thesis delves into the exploration of homomorphic encryption schemes and their application to machine learning algorithms. It provides a comprehensive survey of the literature surrounding homomorphic encryption, presenting the theory behind it and examining its application through various machine learning algorithms.

### Methodology
The thesis covers the Paillier cryptosystem and the fully homomorphic encryption scheme based on the Learning with Errors (LWE) problem. It includes a detailed exploration of how these encryption schemes can be applied to fundamental machine learning algorithms such as Fisher's Linear Discriminant, Linear Regression, Principal Component Analysis, Decision Trees, and Naive Bayes Classifiers. The study also discusses the necessity of approximating certain calculations due to the limitations of somewhat homomorphic encryption schemes.

### Results & Discussions
Yao discusses the limitations of fully homomorphic encryption, including its security, efficiency, and societal impact. The thesis acknowledges that while homomorphic encryption offers significant advantages, it is not without its challenges. Alternatives to homomorphic encryption, such as Yao's garbled circuits and functional encryption, are surveyed to understand the situations in which homomorphic or fully homomorphic encryption is most advantageous.

### Research Gap or Area of Improvement
The thesis identifies that despite the progress in homomorphic encryption, there are still considerable challenges to overcome, especially regarding the efficiency and practical application of these encryption schemes in real-world scenarios.

## Strengths
The strength of this thesis lies in its comprehensive survey of homomorphic encryption schemes and their applications to machine learning algorithms, providing a solid foundation for further research in this area. 

## Weaknesses
The discussion on the practical limitations and the efficiency of these schemes highlights a significant area for improvement, indicating a need for further research to enhance the applicability of homomorphic encryption in practical machine learning tasks.

## Paper presentation

(This section is optional, only fill it when there's something special about it)

(Please evaluate the paper presentation here. You can include both the good and the bad)

## Thoughts
(Can you do better?)

## Takeaways and questions
(What did you like/dislike about the paper? What did your learn?)
(Questions for discussion?)

### Knowledge
Probabilistic Polynomial Time Algorithms (PPT): A PPT algorithm runs in polynomial time and employs **randomness** in its computations.
Key points:
- It may use true randomness to produce possibly non-deterministic results.
- The “probabilistic” aspect arises because certain outcomes can only be predicted with a certain probability.
PPT algorithms are often used to solve computationally difficult problems efficiently, even though they may have a small chance of producing incorrect results.

Application in Cryptography:
- In cryptography, PPT algorithms play a crucial role.
- Security proofs against adversaries often involve considering a wide range of possible attacks.
- By modeling adversaries as logical machines with resource costs (i.e., algorithms), we can reason about security properties.
- PPT algorithms allow us to explore the trade-offs between efficiency and security.
Remember, while PPT algorithms introduce randomness, they remain powerful tools for solving complex problems within reasonable time bounds.


In mathematics, a negligible function is a function that satisfies the following properties:
Definition: A function μ(x) is considered negligible if, for every positive integer c, there exists an integer N_c such that for all x > N_c, we have: [ \mu(x) < \frac{1}{x^c} ]
Equivalence: Alternatively, we can express the same concept using the following definition: A function is negligible if, for every positive polynomial poly(·), there exists an integer N_{\text{poly}} > 0 such that for all x > N_{\text{poly}}, we have: [ \mu(x) < \frac{1}{\text{poly}(x)} ]

Use in Cryptography:
- In modern complexity-based cryptography, a security scheme is considered provably secure if the probability of security failure (e.g., inverting a one-way function or distinguishing pseudorandom bits from truly random bits) is negligible relative to the input (usually the cryptographic key length).
- The reciprocal-of-polynomial formulation ensures tractability in the asymptotic setting.
- Even if an attack succeeds with negligible probability, repeated polynomial times, the overall success probability remains negligible (the combination of negligibility and polynomial time ensures that cryptographic systems remain secure against practical attacks, even if individual events have tiny probabilities of success.).
- Practical security parameters are often chosen to ensure probabilities are smaller than specific thresholds (e.g., 2^(-128)).
Remember, negligible functions play a crucial role in cryptographic proofs and provide a way to reason about security properties in a mathematically rigorous manner.


CPA-security is a stronger standard than EAV-security.
CCA-security is a stronger standard than CPA- or EAV-security and implies them both.


homomorphic encryption schemes have to be malleable because we allow the computation of various functions over the ciphertexts.
Malleability is a requisite characteristic of HE schemes, enabling them to support computations on encrypted data. This controlled malleability is what distinguishes HE from other encryption paradigms and is key to its utility in secure data processing and analysis applications. However, it's important to differentiate this functional malleability from the uncontrolled malleability that might be exploited in traditional encryption schemes. In HE, the malleability is a feature that enables computation while still aiming to maintain the confidentiality and integrity of the data.

Any malleable encryption scheme cannot be secure against adaptive chosen-ciphertext attacks


The Learning with Errors (LWE) problem is a fundamental mathematical concept widely used in cryptography to create secure encryption algorithms1. Let’s dive into the details:

Definition:
In LWE, secret information is represented as a set of equations with errors. Essentially, it’s a way to hide the value of a secret by introducing noise to it.
More technically, LWE involves inferring a linear function over a finite ring from given samples, some of which may be erroneous.
Here’s how it works:
- Let’s denote the ring of integers modulo (q) as (\mathbb{Z}_q), and let (\mathbf{s}) be an unknown linear function.
- The input to the LWE problem consists of pairs ((\mathbf{a}, t)), where (\mathbf{a}) is a vector chosen uniformly from (\mathbb{Z}_q^n), and (t = \langle \mathbf{a}, \mathbf{s} \rangle / q + e).
- The deviation from the equality is determined by a known noise model.
- The goal is to find the function (\mathbf{s}) (or a close approximation) with high probability.

