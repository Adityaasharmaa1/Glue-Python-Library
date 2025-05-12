# Glue-Python-Library

CMD
docker run -it amazonlinux:2


yum update -y
yum install -y python3 python3-pip zip


mkdir /tmp/deps
pip3 install python-gnupg -t /tmp/deps/


cd /tmp/deps
zip -r9 /tmp/python-gnupg.zip .


open new CMD
docker ps
docker cp <container_id>:/tmp/python-gnupg.zip .

