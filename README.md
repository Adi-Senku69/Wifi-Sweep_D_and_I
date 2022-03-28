# WifiSweep
Automated capturing & sorting of WPA & WPA2 password Hashes using hashcat & hcxdumptool.

Automatically creates file with wifi name & captured hash of matching mac addresses.

to delete files in terminal -> sudo rm -R WifiSweep/session name

Make sure your wifi adapter supports monitor mode. 

# For wordlist cracking
hashcat -m 22000 -o password.txt YOURFILENAMEHERE.hc22000 /usr/share/wordlists/rockyou.txt

#For brute-force cracking
hashcat -m 22000 hash.hc22000 -a 3 ?d?d?d?d?d?d?d?d

# for brute forcing with increments 
hashcat -m 22000 hash.hc22000 -a 3 --increment --increment-min 8 --increment-max 18 ?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d

more info about hashcat : https://hashcat.net/hashcat/
more info about hcxdumptool : https://en.kali.tools/?p=841
Youtube Tutorial: https://youtu.be/xFT-1oJLVmo
