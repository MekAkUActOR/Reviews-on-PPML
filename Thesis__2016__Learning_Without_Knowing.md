# Haowen (Date)

# Paper information
(Please use comma as a separator for authors)
(For the venue use the abbreviated conference/journal name: e.g., MICRO 2019)
(Use as many keywords as you wish and don't make them too general)

- Title: Learning Without Knowing: Applying Homomorphic Encryption to Machine Learning Algorithms
- Authors: Yao
- Venue: Thesis
- Keywords: 

# Paper content
## Summary
(What is the problem the paper is trying to solve?)
(What are the key ideas and insights of the paper?)
(What are the key mechanisms and contributions?)
(What are the key conclusions?)

## Strengths
(Please evaluate the *work*, not the *presentation*)

## Weaknesses
(Please evaluate the *work*, not the *presentation*)

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
