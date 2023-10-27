# Background Information

I thought it would be fun to make a sort of storyboard which depicts a hypothetical scenario which is heavily inspired by course work I have recently completed as per my current cyber-security studies. The scenario involves implementing a (site-to-site and client-to-site) VPN solution within the premises of Moonbeam P.D, a police force agency located in the city of Miami.

## Hiring Process and Scope of Work

I recieved an email from Moonbeam P.D expressing their desire to implement a new firewall solution facilating a client-to-site and site-to-site VPN to allow their staff to access internal resources from remote operations and offices.
![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/22d70e58-27ea-47fb-b518-e6e4e9c42a83)

Moonbeam has attatched their cryptographic policy and stated that the solution must meet a level of compliance with the encryption algorithmns, hashing functions, key exchange protocols and authentication methods stated within; it has been identified that the following cryptography be used:

- "AES-Compatible" or "Partially-AES-Compatible" Encryption Algorithmns.
- SHA256 Hashing Function (as per NIST's recommendation).
- IKEv2 with Diffie-Hellman Group 14 (2046 bits) for Key Exchanges.
- SSL with Signed Certificates for Server and User Authentication (client-to-site VPN).
- Complex Pre-Shared Key for Gateway Authentication (site-to-site VPN)

 
