# VoLTE IPSEC decoder

Useful tool if you need to look into Gm trace from VoLTE device. 
The output result is esp_sa file for wireshark, which contains ESP security associations of established ipsec connections over Gm.
It's not magic, ipsec keys are derived from Mw trace (CK,IK of HSS response). That's why input pcap file must contains Gm AND Mw frames altogether.
