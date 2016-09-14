# VoLTE IPSEC decoder

Useful tool if you need to look into Gm trace from VoLTE device. 
The output result is esp_sa file for wireshark, which contains ESP security associations of established ipsec connections over Gm.
It's not magic, ipsec keys are derived from Mw trace (CK,IK of HSS response). That's why input pcap file must contains Gm AND Mw frames altogether.

# Usage
run:  
./parse_tshark_v1.py filename.pcap  

output is in esp_sa file:  
```
"IPv4","*","*","0x000ca2ae","AES-CBC [RFC3602]","0xc02b5a7c2dfec5ccbb48f1cfb1b0e5ff","HMAC-MD5-96 [RFC2403]","0x71f2b1e1f42fac8bc90b9163b534ba96"
"IPv4","*","*","0x000ca2af","AES-CBC [RFC3602]","0xc02b5a7c2dfec5ccbb48f1cfb1b0e5ff","HMAC-MD5-96 [RFC2403]","0x71f2b1e1f42fac8bc90b9163b534ba96"
"IPv4","*","*","0x81ac3768","AES-CBC [RFC3602]","0xc02b5a7c2dfec5ccbb48f1cfb1b0e5ff","HMAC-MD5-96 [RFC2403]","0x71f2b1e1f42fac8bc90b9163b534ba96"
"IPv4","*","*","0x814bf561","AES-CBC [RFC3602]","0xc02b5a7c2dfec5ccbb48f1cfb1b0e5ff","HMAC-MD5-96 [RFC2403]","0x71f2b1e1f42fac8bc90b9163b534ba96"
```
