Build Image
==========

docker build -t myubuntu:latest -f DockerFile.yml .

Run Daemon
==========

docker run -d --name u1 -p 53022:22 myubuntu:latest

SSH into Daemon
================

ssh root@192.168.99.100 -p 53022
