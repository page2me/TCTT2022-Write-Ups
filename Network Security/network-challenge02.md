$ tshark -r network_security02.pcap -Y "frame contains PK" -T fields -e tcp.stream

19836
20089
20123
20123
20129

$ tshark -r network_security02.pcap -Y "frame contains PK" -qz follow,tcp,raw,20129 | tail -n 2 | head -n -1 | xxd -r -p > secret.zip

$ fcrackzip -u -D -p rockyou.txt secret.zip

PASSWORD FOUND!!!!: pw == P@ssw0rd

$ 7z x secret.zip -pP@ssw0rd

$ strings secret

tctt2022{Welcome_R00t_T3ln3t}
