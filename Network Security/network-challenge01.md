$ tshark -r network_security01.pcap -Y "frame contains PK" -T fields -e tcp.stream

20097

$ tshark -r network_security01.pcap -Y "frame contains PK" -z follow,tcp,raw,20097 | tail -n-5 | head -n-1 | xxd -r -p> secret.zip

$ fcrackzip -u -D -p rockyou.txt secret.zip

PASSWORD FOUND!!!!: pw == password

$ 7z x secret.zip -ppassword

$ strings secret

tctt2022{Steal_Data_via_FTP}
