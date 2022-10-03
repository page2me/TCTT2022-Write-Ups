$ tshark -r network_security02.pcap -Y "frame contains PK" -T fields -e data | tail -n -1 | xxd -r -p > secret.zip

$ fcrackzip -u -D -p rockyou.txt secret.zip

PASSWORD FOUND!!!!: pw == P@ssw0rd

$ 7z x secret.zip -pP@ssw0rd

$ strings secret

tctt2022{Welcome_R00t_T3ln3t}
