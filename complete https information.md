## Introduction

The server's private key is used to decrypt the session key that the client sends during the initial connection, and the server's public key is used to encrypt messages that are sent to the client during the session. 

The client's private key is used to decrypt messages that are sent from the server during the session, and the client's public key is used to encrypt messages that are sent to the server.

When the client connects to a website using HTTPS,  

- The server sends its public key to the client as part of the **SSL/TLS handshake** process. 
- The client then uses the server's **public key** to encrypt the session key, which is sent back to the server. 
- Once the server receives the encrypted session key, it uses its **private key** to decrypt it and obtain the original session key.

During the session, both the client and the server use the session key to encrypt and decrypt data that is transmitted between them. This ensures that the data cannot be intercepted or tampered with by unauthorized parties.

So, both the client and server have their own set of private and public keys, and they use them in combination with the session key to establish a secure and private connection for transmitting data over the internet.

## Server public keys

- When a client (such as your web browser) connects to a website using HTTPS, the server sends its public key to the client as part of the SSL/TLS handshake process. The client then uses the server's public key to encrypt a secret key called the session key, which is used to encrypt and decrypt data that is transmitted between the client and server during the session.

- The server's public key is used in this way because it is widely available and can be freely distributed. By contrast, the server's private key is kept secret and is never shared with anyone else. This allows the server to ensure that only authorized parties can decrypt the session key and access the data that is transmitted during the session.

- In other words, the server's public key is used to establish a secure and private communication channel between the client and server, without revealing the private key that is used to decrypt the data. This helps to prevent eavesdropping, data tampering, and other types of attacks that could compromise the security and privacy of the communication.

- Overall, the server's public key is a crucial component of the HTTPS encryption process, and is used to establish a secure and private connection between the client and server.

## Server private keys

- The server's private key is a critical component of the HTTPS encryption process, and is used to decrypt the session key that is sent by the client during the SSL/TLS handshake process.

- When a client (such as your web browser) connects to a website using HTTPS, the server sends its public key to the client as part of the SSL/TLS handshake process. The client then uses the server's public key to encrypt a secret key called the session key, which is used to encrypt and decrypt data that is transmitted between the client and server during the session.

- The session key is encrypted with the server's public key because it ensures that only the server can decrypt and access the key. Once the session key has been sent to the server, the server uses its private key to decrypt the session key and establish a secure and private communication channel between the client and server.

- The server's private key is kept secret and is never shared with anyone else, as it is crucial for ensuring the security and privacy of the communication. If an attacker were to gain access to the server's private key, they could use it to decrypt the session key and access the data that is transmitted during the session.

- Overall, the server's private key is a crucial component of the HTTPS encryption process, and is used to decrypt the session key that is sent by the client during the SSL/TLS handshake process. This helps to establish a secure and private communication channel between the client and server, and helps to prevent eavesdropping, data tampering, and other types of attacks that could compromise the security and privacy of the communication.

## Client public & private key

> [!NOTE] client private is used by client to encrypt digital certificate
> When the client sends its digital certificate to the server during the SSL/TLS handshake process, it is encrypted using the client's private key. 

However, the server cannot decrypt the digital certificate using the client's private key because it does not have access to the key.

> [!NOTE] client public key is used by server to decrypt client's digital certificate
> Instead, the server uses the client's public key, which is contained in the digital certificate, to decrypt the certificate of the client. 

This is possible because the client's digital certificate contains both the client's public key and its encrypted digital signature, which can be verified by the server using the client's public key.

**Here's how the process works**:

1.  The client generates a key pair consisting of a private key and a public key.
    
2.  The client creates a digital certificate that contains its public key, as well as information about the client's identity and the certificate authority that issued the certificate.
    
3.  The client encrypts the digital certificate using its private key. This ensures that only the client can decrypt and access the certificate.
    
4.  When the client connects to the server using HTTPS, it sends its digital certificate to the server during the SSL/TLS handshake process.
    
5.  The server uses the certificate authority's public key to verify the authenticity of the client's digital certificate.
    
6.  If the digital certificate is valid, the server extracts the client's public key from the certificate and uses it to decrypt the encrypted digital signature.
    
7.  The server then compares the decrypted digital signature with a freshly computed digital signature of the same data. If the two signatures match, the server knows that the client is authentic and establishes a secure and private communication channel with the client.
    

	So, to summarize, the server does not decrypt the client's digital certificate directly using the client's private key. Instead, it uses the client's public key, which is contained in the digital certificate, to decrypt the certificate and verify its authenticity.

## Digital certificate

A digital certificate, also known as a public key certificate, is an electronic document that is used to establish the identity of an entity, such as a person, organization, or device, in a digital communication.

The digital certificate contains the following information:

1.  **Public key**: A public key is a cryptographic key that is used for encryption and decryption. It is included in the certificate and is used by the recipient to encrypt messages that can only be decrypted by the certificate holder, who possesses the corresponding private key.
    
2.  **Issuer**: The issuer of the certificate is the organization or authority that issues the certificate. This information is included in the certificate to establish trust and ensure that the certificate is valid.
    
3.  **Subject**: The subject of the certificate is the entity that is being identified, such as a person or an organization. The subject's name and other identifying information are included in the certificate.
    
4.  **Validity period**: The certificate contains a validity period, which specifies the period during which the certificate is considered valid. This helps prevent the use of expired or revoked certificates.
    
5.  **Digital signature**: The certificate includes a digital signature that is used to ensure the authenticity of the certificate. The signature is generated using the private key of the certificate issuer and is used to verify the integrity of the certificate and the identity of the certificate holder.
    
6.  **Certificate Authority (CA)**: The certificate authority is the organization that issues and verifies digital certificates. The CA's digital signature is included in the certificate, which is used by the recipient to verify the authenticity of the certificate.


Overall, the digital certificate provides a means of verifying the identity of the entity that is being communicated with in a secure and private manner.