# TLS protocol
TLS protocol in [wiki](https://en.wikipedia.org/wiki/Transport_Layer_Security) <br>
TLS1.0 [RFC2246](https://datatracker.ietf.org/doc/rfc2246/?include_text=1) <br>
TLS1.1 [RFC4346](https://datatracker.ietf.org/doc/rfc4346/?include_text=1) <br>
TLS1.2 [RFC5246](https://datatracker.ietf.org/doc/rfc5246/?include_text=1) <br>
TLS1.3 [RFC8446](https://datatracker.ietf.org/doc/rfc8446/?include_text=1) <br>

[RFC6125](https://datatracker.ietf.org/doc/rfc6125/?include_text=1) Representation and Verification of Domain-Based Application Service Identity within Internet Public Key Infrastructure Using X.509 (PKIX) Certificates in the Context of Transport Layer Security (TLS) <br>

## Cryptograph
### RSA
PKCS#1 RSA Encryption Version 1.5 [RFC2313](https://datatracker.ietf.org/doc/rfc2313/?include_text=1) <br>

## Attack
### Renegotiation Attack
[Understanding the TLS Renegotiation Attack](http://www.educatedguesswork.org/2009/11/understanding_the_tls_renegoti.html) <br>
TLS Renegotiation Indication Extension [RFC5746](https://datatracker.ietf.org/doc/rfc5746/?include_text=1) <br>
	
### FREAK (Factoring RSA Export Keys)
FREAK ("Factoring RSA Export Keys") is a security exploit of a cryptographic weakness in the SSL/TLS protocols introduced decades earlier for compliance with U.S. cryptography export regulations. These involved limiting exportable software to use only public key pairs with RSA moduli of 512 bits or less (so-called RSA_EXPORT keys), with the intention of allowing them to be broken easily by the National Security Agency (NSA), but not by other organizations with lesser computing resources. However, by the early 2010s, increases in computing power meant that they could be broken by anyone with access to relatively modest computing resources using the well-known Number Field Sieve algorithm, using as little as $100 of cloud computing services. Combined with the ability of a man-in-the-middle attack to manipulate the initial cipher suite negotiation between the endpoints in the connection and the fact that the Finished hash only depended on the master secret, this meant that a man-in-the-middle attack with only a modest amount of computation could break the security of any website that allowed the use of 512-bit export-grade keys. While the exploit was only discovered in 2015, its underlying vulnerabilities had been present for many years, dating back to the 1990s. <br>
[wiki description](https://en.wikipedia.org/wiki/FREAK) <br>
OpenSSL has the identifier [CVE-2015-0204](https://www.cvedetails.com/cve/CVE-2015-0204/?q=+CVE-2015-0204) <br>
Microsoft's vulnerability in SChannel is [CVE-2015-1637](https://www.cvedetails.com/cve/CVE-2015-1637/?q=CVE-2015-1637) <br>
Apple's vulnerability in Secure Transport is [CVE-2015-1067](https://www.cvedetails.com/cve/CVE-2015-1067) <br>

### DROWN (Decrypting RSA with Obsolete and Weakened eNcryption)
The DROWN (Decrypting RSA with Obsolete and Weakened eNcryption) attack is a cross-protocol security bug that attacks servers supporting modern TLS protocol suites by using their support for the obsolete, insecure, SSL v2 protocol to leverage an attack on connections using up-to-date protocols that would otherwise be secure. DROWN can affect all types of servers that offer services encrypted with TLS yet still support SSLv2, provided they share the same public key credentials between the two protocols. Additionally, if the same public key certificate is used on a different server that supports SSLv2, the TLS server is also vulnerable due to the SSLv2 server leaking key information that can be used against the TLS server. <br>
[wiki description](https://en.wikipedia.org/wiki/DROWN_attack) <br>
[CVE-2016-0800](https://www.cvedetails.com/cve/CVE-2016-0800/?q=+CVE-2016-0800) <br>
[Chosen-ciphertext attack](https://en.wikipedia.org/wiki/Chosen-ciphertext_attack) <br>
[Man-in-the-middle attack](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) <br>
