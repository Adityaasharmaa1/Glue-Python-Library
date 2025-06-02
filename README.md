Docker Spin up

using CMD - docker run -it --rm -v %cd%:/data amazonlinux:2
or if using linux or mac - docker run -it --rm -v $(pwd):/data amazonlinux:2

yum update -y
yum install -y gnupg2


gpg2 --full-generate-key (if doesn't work use below command)
gpg2 --gen-key


Options to choose while e=generating keys
- RSA and RSA
- Choose expiry
- Choose realname - any persons name or team name
- id - choose any persons email id or teams email id 
- enter passphrase twice

Export keys
-gpg2 --armor --export <your_email_or_keyid> > /data/public_key.asc
-gpg2 --armor --export-secret-keys <your_email_or_keyid> > /data/private_key.asc


to convert to base64 for storage into scerets
 - base64 /data/private_key.asc | tr -d '\n' > /data/private_key_base64.txt

