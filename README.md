# Background Information

I thought it would be fun to make a sort of storyboard which depicts a hypothetical scenario which is heavily inspired by course work I have recently completed as per my current cyber-security studies. The scenario involves being hired to implement a (site-to-site and client-to-site) VPN solution within the premises of Moonbeam P.D, a police force agency located in the city of Miami.

For this whole storyboard, I will refer to myself as ACA (Average Cyber Agency).

## Hiring Process and Job Information

I recieved an email from Moonbeam P.D expressing their desire to implement a new firewall solution facilating a client-to-site and site-to-site VPN to allow their staff to access internal resources from remote operations and offices.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/22d70e58-27ea-47fb-b518-e6e4e9c42a83)

Moonbeam has attatched their cryptographic policy and stated that the solution must meet a level of compliance with the encryption algorithmns, hashing functions, key exchange protocols and authentication methods stated within; it has been identified that the following cryptography be used:

- "AES-Compatible" or "Partially-AES-Compatible" Encryption Algorithmns.
- SHA256 Hashing Function (as per NIST's recommendation).
- IKEv2 with Diffie-Hellman Group 14 (2046 bit modulus) for Key Exchanges.
- SSL with Signed Certificates for Server and User Authentication (client-to-site VPN).
- Complex Pre-Shared Key for Gateway Authentication (site-to-site VPN)

As per their request, I sent back an email providing details of the work to be completed and a price quote.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/50156172-a1fa-40d1-b8c4-9d3e2b95eea7)

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/aac3420e-17da-4455-af94-d9d2c3f70b44)

## The Solution

As was mentioned previously, Moonbeam P.D is looking for a site-to-site and client-to-site VPN solution to accommedate their organisation's current network 'scope' which consists of a remote office network (office B), an internal network and the various networks remote workers will be connecting from. 

ACA has recognised that Moonbeam P.D has approximately 300 staff and has chosen a firewall appliance that suits - pfSense NetGate 8200 Max. The pfSense NetGate 8220 Max has been chosen as it is a high-end firewall appliance made for medium-large organisations and is compatible with the cryptographic policy - that of supporting the outlined cryptography and authentication methods.

The following topology has been created to show ACA's proposed solution, outlining an IPsec site-to-site VPN between the internal LAN and office B, and a SSL client-to-site VPN between the internal LAN and remote workers.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/92db4c9c-9711-4ec9-9085-e12c75068217)









 
