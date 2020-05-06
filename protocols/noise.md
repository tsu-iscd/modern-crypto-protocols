# Noise

## Noise Protocol
* [David Wong. The Noise Protocol Framework](https://www.youtube.com/watch?v=ceGTgqypwnQ)
* [David Wong. Modern Session Encryption](https://permutationbasedcrypto.org/2018/slides/David_Wong.pdf)
* [Noise Spec](https://noiseprotocol.org/noise.html)
* [Noise Wiki](https://github.com/noiseprotocol/noise_wiki/wiki)


## WireGuard

### Basic Properties
* UDP-based
* 1-RTT
* Key confirmation
* Anti-replay
* Cookies
* No ratcheting
* No message keys
* Key rotation every 2 minutes
* no PKI

### Silence
* One design goal of WireGuard is to avoid storing any state prior to authentication and to not send any responses
to unauthenticated packets.
* No state, no responses for unauthorized peers.
* WireGuard is invisible to illegitimate peers and network scanners.
* This means that the first message has to authenticate the initiator.
* So the first message can be replied bu an attacker
* To prevent this timestamp is used :  The responder keeps track of the greatest timestamp received per peer and
discards packets containing timestamps less than or equal to it.
* Integrity: This timestamp ensures that an attacker may not disrupt an current session between initiator and responder via replay attack.
* But only if responder's public key is unknown.
* "While the public key of the responder itself is not secret, it is sufficiently secret within this attack model, in
which the goal is to ensure stealthiness of services, and so knowing the responder’s public key is sufficient proof
for already knowing of its existence"
* Mac1 field is used

### DoS Mitigation and Cookies
* If the responsed is under load it may send a coookie
* The responder maintains a secret random value that changes every two minutes.
* A cookie is simply the result of computing a MAC of the initiator’s source IP address using this changing secret as the MAC key. 
* The initiator, when resending its message, sends a MAC of its message using this cookie as the MAC key
* Mac2 field is used

### KCI Resistance
After a handshake is completed, with a message from initiator to responder and then responder back to initiator, the initiator may then send encrypted session packets, but the responder cannot. The responder must wait to use the new session until it has recieved one encrypted session packet from the initiator, in order to provide key confirmation.

```
IK:
<-s
…
-> e, es, s, ss
<- e, ee, se
```
Why is that?

An attacker knows S_B_priv. So the attacker can send first message using an ephemeral key pair. But the attacker does not know S_A_priv. Bob uses `se` on the second message: to do that he needs Alice's public static key and ephemeral key. So Alice will have to use private static key. To prove that Alice knows private static key she has to send a transport message. 

### Transport
* Since WireGuard operates over UDP, messages can sometimes arrive out of order. 
* For that reason a sliding window to keep track of received message counters is used

## nQUIC

### Basic properties
* 1-RTT and 0-RTT
* Key ratcheting
* no PKI

## Links
* [libreswan: IPsec Implemented Standards](https://libreswan.org/wiki/RFC_List)
