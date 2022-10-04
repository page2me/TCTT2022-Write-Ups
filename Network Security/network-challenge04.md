$ tshark -r network_security04.pcap --export-objects http,network_security04 | grep secret.zip

26157 359.529163 212.192.246.16 → 202.139.203.149 HTTP 194 GET /secret/zip HTTP/1.1

26159 359.529697 212.192.246.16 → 202.139.203.149 HTTP 199 GET /secret/zipfiles HTTP/1.1

26161 359.530216 212.192.246.16 → 202.139.203.149 HTTP 195 GET /secret/zips HTTP/1.1

26601 578.530216 212.192.246.16 → 202.139.203.149 HTTP 454 GET /download/secret.zip HTTP/1.1

$ 7z x secret.zip

$ ls -l dev | sort| head

-rwxrwxr-x 1 root root 600 Sep 11 08:01 test_69.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_100.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_10.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_11.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_12.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_13.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_14.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_15.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_16.txt

-rwxrwxr-x 1 root root 602 Sep 11 08:01 test_17.txt

$ cat dev/* | sort | uniq | awk '{print "echo \""$1"\"|base64 -d|base64 -d|base64 -d|base64 -d|base64 -d|base64 -d|base64 -d|base64 -d|base64 -d"}'| bash


base64: invalid input

base64: invalid input

base64: invalid input

base64: invalid input

base64: invalid input

tctt2022{M3s$age_Secr3t_1n_C0rr3ct_F!l3}

tctt2022{M3s$ag

base64: invalid input

base64: invalid input

base64: invalid input

base64: invalid input

base64: invalid input

tctt2022{M3s$ag
