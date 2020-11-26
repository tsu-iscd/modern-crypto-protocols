# Cryptographic Protocols 2020

## 9/3/2020: Introduction

## 9/10/2020: Key Agreement Protocols: Goals, Notions, Primitives

Readings:
* [Handbook of Applied Cryptography. Key Establishment Protocols](http://cacr.uwaterloo.ca/hac/about/chap12.pdf)
* [Shafi Goldwasser. Mihir Bellare. Lecture Notes on Cryptography. Chapter 11](http://www.cs.tufts.edu/comp/165/papers/Goldwasser-Bellare-notes-cryptography.pdf)
* [A Computational Introduction to Number Theory and Algebra: Chapter 11](https://www.shoup.net/ntb/ntb-v2.pdf)
* [RFC 2631. Diffie-Hellman Key Agreement Method](https://tools.ietf.org/html/rfc2631)
* [RFC 3526. More Modular Exponential (MODP) Diffie-Hellman groups for Internet Key Exchange (IKE)](https://tools.ietf.org/html/rfc3526)

## 9/17/2020: Basic Attacks on Diffie-Hellman Protocols

Readings:
* [Imperfect Forward Secrecy: How Diffie-Hellman Fails in Practice](https://weakdh.org/imperfect-forward-secrecy-ccs15.pdf)
* [In search of CurveSwap: Measuring elliptic curve implementations in the wild](https://i.blackhat.com/eu-18/Thu-Dec-6/eu-18-Valenta-In-Search-Of-CurveSwap-Measuring-Elliptic-Curve-Implementations-In-The-Wild-wp.pdf)

Assignments:
* [Implement Diffie-Hellman](https://cryptopals.com/sets/5/challenges/33)
* [Implement a MITM key-fixing attack on Diffie-Hellman with parameter injection](https://cryptopals.com/sets/5/challenges/34)
* [Implement DH with negotiated groups, and break with malicious "g" parameters](https://cryptopals.com/sets/5/challenges/35)
* [Implement Subgroup-Confinement Attack](https://toadstyle.org/cryptopals/57.txt)

## 9/24/2020: Authenticated Key Exchnage

Readings:
* [Boneh-Shoup. Chapter 21](https://toc.cryptobook.us/book.pdf)
* [HMQV: A High-Performance Secure Diffie-Hellman Protocol](https://eprint.iacr.org/2005/176.pdf)

## 10/1/2020: Authenticated Key Exchnage

Readings:
* [Boneh-Shoup. Chapter 21](https://toc.cryptobook.us/book.pdf)

Assignments:
* [Implement Pollard's Method for Catching Kangaroos](https://toadstyle.org/cryptopals/58.txt)

## 10/8/2020: Authenticated Key Exchnage

Readings:
* [Boneh-Shoup. Chapter 21](https://toc.cryptobook.us/book.pdf)

## 10/15/2020: Introduction to Elliptic Curve Cryptography

Readings:
* [Boneh-Shoup. (Chapter 15, sections 15.1 - 15.3)](https://toc.cryptobook.us/book.pdf)

## 10/22/2020: Attacks on Elliptic Curve Cryptography 

Readings:
* [Breaking the Bluetooth Pairing: Fixed Coordinate Invalid Curve Attack](http://www.cs.technion.ac.il/~biham/BT/bt-fixed-coordinate-invalid-curve-attack.pdf)
* [SafeCurves: choosing safe curves for elliptic-curve cryptography](https://safecurves.cr.yp.to/twist.html)

Assignments:
* [Elliptic Curve Diffie-Hellman and Invalid-Curve Attacks](https://toadstyle.org/cryptopals/59.txt)
* [Single-Coordinate Ladders and Insecure Twists](https://toadstyle.org/cryptopals/60.txt)

## 10/29/2020: HMQV: A High-Performance Secure Diffie-Hellman Protocol

Readings:
* [HMQV: A High-Performance Secure Diffie-Hellman Protocol](https://eprint.iacr.org/2005/176.pdf)

## 11/19/2020: X3DH

Readings:
* [The X3DH Key Agreement Protocol](https://signal.org/docs/specifications/x3dh/)

## 11/26/2020: Double Ratchet

Readings:
* [The Double Ratchet Algorithm](https://signal.org/docs/specifications/doubleratchet/)

## 12/3/2020: Noise: Principles, Mechanics and Semantics

Readings:
* [Noise Protocol Framework](http://www.noiseprotocol.org/). Sections 1-6, 9, 13-14.

## 12/10/2020: Noise: Advanced Features and Security Properties

Readings:
* [Noise Protocol Framework](http://www.noiseprotocol.org/). Sections 7-8, 10-11, 18.


## Someday

## KEM, PQ-KEM

Readings:
* [Strongly Secure Authenticated Key Exchange from Factoring, Codes, and Lattices](https://eprint.iacr.org/2012/211.pdf)

## WireGuard and PQ-WireGuard

Readings:
* [WireGuard: Next Generation Kernel Network Tunnel](https://www.wireguard.com/papers/wireguard.pdf)
* [Post-quantum WireGuard](https://eprint.iacr.org/2020/379.pdf)

## Identification Protocols

Readings:
* [Boneh-Shoup. Chapter 18](https://toc.cryptobook.us/book.pdf)

### Zero-Knowledge

Readings:
* [Boaz Barak's notes on Zero Knowledge](https://www.cs.princeton.edu/courses/archive/fall07/cos433/lec15.pdf)
* Benny Pinkas. Sigma Protocols ([slides](http://cyber.biu.ac.il/wp-content/uploads/2018/08/WS-19-11-sigma-protocols-winter-school-2019-1.pdf), [video](https://www.youtube.com/watch?v=XT1Pad0DM24))
* [Boneh-Shoup. Chapter 19](https://toc.cryptobook.us/book.pdf)

### Introduction to MPC

Readings:
* [A Pragmatic Introduction to Secure Multi-Party Computation](https://www.cs.virginia.edu/~evans/pragmaticmpc/pragmaticmpc.pdf)
* [Anca Nitulescu. Introductioon to MPC](https://www.di.ens.fr/~nitulesc/files/slides/MPC-intro.pdf)

### The Double-Ratchet Algorithm

Video:
* [The double-ratchet algorithm: its security and privacy](https://www.youtube.com/watch?v=PSMqfPCM6_4&feature=emb_logo)

### Introduction to zk-SNARK

Readings:
* [Anca Nitulescu. zk-SNARKs: A Gentle Introduction](https://www.di.ens.fr/~nitulesc/files/Survey-SNARKs.pdf)
