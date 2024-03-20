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

#### HSM Keys
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

