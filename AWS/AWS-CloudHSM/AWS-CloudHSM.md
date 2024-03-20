# AWS CloudHSM
- Use Client SDKs to integrate with the HSMs.
- You can use Client SDK Logs, AWS CloudTrail, audit logs and Amazon CloudWatch to monitor.

### AWS CloudHSm Clusters
- Collection of individual HSMs that AWS CloudHSM keeps in sync.
- When you perform a task or operation in one HSM in a cluster. The other HSMs in that cluster are automatically kept up to date.
- You set the number of HSMs in you cluster across multiple availability zones for availability, durability and scalability goals.
- Can create a a cluster with 1 to 28 HSms
- Default limit is 6 HSms per account per region.

### HSM Users
- YO DO NOT use AWS Identity and IAM or IAM policies to access resources.
- You use HSM Users directly on HSMs un your AWS CloudHSM cluster.
- HSM User has types that determines which operations can perform on the HSM.
- Each HSM authenticates each HSM User by means of credentials that were defined using CloudHSM CLI.

### HSM Keys
AWS CloudHSM allows you the follow actions for the encryption keys in an single tenant HSMs that are in your cluster:
    - Generate
    - Store
    - Manage
- Keys can be exported from or imported into AWS CloudHSM.
- keys can be symmetric or asymmetric.
- key can be:
  - Sessiona keys (ephemeral keys) for single sessions
  - Token keys (presistent keys) for long-term use

### Client SDKs
- Used by the applications you develop to perform cryptographic operations with AWS CloudHSM.
- Includes:
  - PKCS #11
  - JCE provider
  - OpenSSL Dynamic Engine
  - Cryptography API: Next Generation an Key storage provider for Microsoft Windows.

### ZPK (Zone Master Key)
- Also known as an Interchange key (IK).
- Is a key-encrypting key which is distributed manually between two communicating sites, within a shared network, in order that further keys can be exchanged automatically.
- The ZMK is used to encrypt keys of a lower level (e.g. ZPK) for transmission.

The ZMK is exchanged using secured methods and Split knowledge policy. The IK is split into two components that are sent by two separate physical couriers to two nominated Security Officers of the other party. This is one of the most secure way to do it since no single person gains knowledge of the clear ZMK.

Here is the detailed Process. please note values indicated here are for testing only, in live environment the values will be exchanged securely.

### ZPK (Zone PIN Key)
- Also known as a A PIN Protection Key (PPK).
- Is a data encrypting key which is distributed automatically and is used to encrypt PINs. 
- For security and protocol reasons the HSM where this key generated, never exposes the ZPK in clear. But it can be exported using another key called ZMK (Interchange Key). In this context exports actually means use the ZMK Key to encrypt the ZPK and give back to the user.