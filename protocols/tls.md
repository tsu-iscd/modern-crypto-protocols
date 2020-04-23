# TLS

## TLS 1.2

### Connections
- [Illustrated connection](https://tls.ulfheim.net/)
- [TLS 1.2](https://www.cloudshark.org/captures/26fa735868c1)

### Attacks
- [Triple Handshake Attack](https://mitls.org/pages/attacks/3SHAKE)

## TLS 1.3

### Connections
- [Illustrated connection](https://tls13.ulfheim.net/)
- [0-RTT](https://www.cloudshark.org/captures/64d433b1585a)

### Protocol
- [Protocol Overview](https://www.davidwong.fr/tls13/#section-2)
- [Client Hello](https://tools.ietf.org/html/rfc8446#section-4.1.2)
- [Record Layer](https://tools.ietf.org/html/rfc8446#section-5.1)
- [Cipher Suites](https://tools.ietf.org/html/rfc8446#appendix-B.4)

### Protocol Notes
- Legacy fields (legacy_record_version, legacy_version, legacy_session_id)

#### Downgrade Attack Prevention
The cryptographic parameters should be the same on both sides and should be the same as if the peers had been communicating in the absence of an attack.

1. Finished message.
Both client and server must send a Finished message which contains a MAC over all previous handshake messages, so that both client and server ensure that the negotiated parameters have not been modified in the middle by an attacker.

2. Downgrade prevention mechanism.
```
   TLS 1.3 has a downgrade protection mechanism embedded in the server's
   random value.  TLS 1.3 servers which negotiate TLS 1.2 or below in
   response to a ClientHello MUST set the last 8 bytes of their Random
   value specially in their ServerHello.

   If negotiating TLS 1.2, TLS 1.3 servers MUST set the last 8 bytes of
   their Random value to the bytes:

     44 4F 57 4E 47 52 44 01

   If negotiating TLS 1.1 or below, TLS 1.3 servers MUST, and TLS 1.2
   servers SHOULD, set the last 8 bytes of their ServerHello.Random
   value to the bytes:

     44 4F 57 4E 47 52 44 00

   TLS 1.3 clients receiving a ServerHello indicating TLS 1.2 or below
   MUST check that the last 8 bytes are not equal to either of these
   values.  TLS 1.2 clients SHOULD also check that the last 8 bytes are
   not equal to the second value if the ServerHello indicates TLS 1.1 or
   below.  If a match is found, the client MUST abort the handshake with
   an "illegal_parameter" alert.  This mechanism provides limited
   protection against downgrade attacks over and above what is provided
   by the Finished exchange: because the ServerKeyExchange, a message
   present in TLS 1.2 and below, includes a signature over both random
   values, it is not possible for an active attacker to modify the
   random values without detection as long as ephemeral ciphers are
   used.  It does not provide downgrade protection when static RSA
   is used.
```

### Mechanisms
- [Key Schedule](https://www.davidwong.fr/tls13/#section-7.1)
- [Client ephemeral, server ephemeral, static secret, ephemeral secret](https://mailarchive.ietf.org/arch/msg/tls/Xizqq_zj7gaHJD_6Zg7R7Mp25-I/)
- [OPTLS and TLS 1.3](https://rwc.iacr.org/2016/Slides/rwc16-wee.pdf)
- [Finished Message](https://www.davidwong.fr/tls13/#section-4.4.4)
- [Transcript Hash](https://www.davidwong.fr/tls13/#section-4.4.1)
