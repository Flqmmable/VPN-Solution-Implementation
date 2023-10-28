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

The following topology has been created to show ACA's proposed solution, outlining an IPsec site-to-site VPN between the internal LAN and office B, and a SSL (via OpenVPN) client-to-site VPN between the internal LAN and remote workers.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/92db4c9c-9711-4ec9-9085-e12c75068217)

## Client-to-Site Implementation

I started by setting up the client-to-site VPN on the instace of pfSense facing outward from the internal LAN. I made sure to utilise the identified cryptography in order to stay compliant with Moonbeam P.D's cryptography policy.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/29e55b6a-a2c2-47bd-982b-02796df04c54)

I then went onto create a user for remote workers and created certificates for both server and user authentication. 

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/bf96dabc-d429-492b-9ae7-2be0efcb8908)

## Site-to-Site Implementation

As mentioned before, I will be using IPsec for the client-to-site VPN; with the cryptography policy in mind, I set up the phase 1 and phase 2 negotiation information on both instaces of pfSense - that is, the instance located in office B and the instance located in the internal LAN.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/68effeec-21e0-4f3e-80b4-f48883010555)

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/a2abacb3-d1f2-4106-be78-b0a0f9c47089)

After this, both firewalls/gateways were able to authenticate each other to create a bidirectional access of internal network resources.

## Solution in Action

This part of the storyboard will show the functionality of the implemented VPN solution.

Via newly established client-to-site VPN, remote workers will now be able to access resources on the internal LAN from wherever they are by downloading an OpenVPN client, installing relevant user certificates and logging in with valid user credentials.

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/6624068a-ddc7-418d-94df-7de243e03a0b)

![image](https://github.com/Flqmmable/VPN-Solution-Implementation/assets/129753283/675c46d4-67d4-40a5-9aa4-f01c107a51c6)


















 
