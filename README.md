# Open Charging Community PKI

Public Key Infrastructures (PKIs) play a crucial role in ensuring the security and trustworthiness of digital communications.
This is especially important as whereever numerous competing companies, service providers, manufacturers, and other entities
have to coexist, distrust among each other can be a substantial barrier.

Unfortunately the traditional X.509 certificate standard is limited to a tree like structure having a single entity at its root
and a direct chain of trust from the root to each leaf entity. Nevertheless, the reality of relationships within e-mobility are
not simply one-to-one but involve multiple parties and are often many-to-many. This requires a more flexible and robust approach
to secure communication and trust. Therefore deviating from the traditional X.509 certificate standard will provide significant
benefits, given the inherent complexities of the sector and its daily politics.

Rather than modelling the e-mobility secotor as a linear hierarchy, it can better be represented as a graph of interconnected
enities, where multiple signatures per certificate are used to reflect and secure the complex, many-to-many relationships
inherent to the e-mobility ecosystem. Multi-signature certificates can capture the nuanced and multi-faceted relationships in
e-mobility. They allow for more than one party to sign and verify a certificate, which is particularly useful when multiple
entities need to agree on the authenticity of an entity or the validity of an operation. This multi-signature feature ensures
that a single compromised key does not lead to a system-wide security breach, enhancing the overall security posture of the
e-mobility ecosystem.

This new, graph-based PKI concept places an emphasis on collaborative security via a quorum of multiple private keys belonging
to various stakeholders at its center. In practice, it means that core certificates within the system will be signed by
multiple parties, reflecting their collective approval or agreement. This quorum-based validation principle not only boost
security but also introduces a unique sense of shared responsibility and trust among the diverse entities within the e-mobility
ecosystem. By requiring a majority of signatures, it ensures that no single entity can unilaterally validate a certificate,
preventing any potential misuse or compromise of a single private key from causing widespread damage.

In conclusion, this unique PKI with multi-signature quorum-based certificates represents a more accurate, secure, and flexible
approach to managing and securing the complex web of relationships in the e-mobility ecosystem. This approach moves away from the
limitations of the traditional X.509 model, embracing a graph-based representation of reality to ensure secure, trusted
digital communications in e-mobility.


## Fundamental Quorum

The following three [secp521r1](https://neuromancer.sk/std/nist/P-521) public keys define the fundamental 2/3 quorum.    
The encoding is base64.

```
Public Key A: BAB8pJPtTwPHgsb3xMdTXLq9kq6TzpPEVpVHkJNyOAthvMTYRK2tsXveD97P1yI5zAEb4yF+l5yjyJsB307DX5KNpwEznHYoH32bs30LnipUmJ88ldN4M5N6Helijc65aRCqAbfr1kUVaOQjLvTYWOx8AopRhFLyrWEB2lH5b/7tXJpf+w==
Public Key B: BAGJ97u5yXD8ApIWfK1vL4ceWj2vSFinkJcqs4lrU7eXYHvCtljpeOCM3pOs1yGJbyMPHUq/fLjO6HXvQcR6SndvYADXiPdTRL/2pJX01Cxuy0CRxQqyopx2eWIHoS6zd1XwxL/4+l2mxeA7UkwW/y/QUQz2JqCGwJ/90gAiPfqGqMu0SQ==
Public Key C: BAD6gAvorknfJRkmjLUPeynVi30aREhVO6H/674n9vW3K1FzaWdtZnDLDl93DlvqsNWvam34AOu3Kw9Xw4ng/NG0rgECAcXIW6OToE48ZSsp6CVRcYat3xgntTS7v2I15kc/4q3cfr40R2hSUYAI7iYgQab49TavfQmUxHBJQx4XeSKphw==
```
