# docker4minecraft
This is my collection of dockerfiles to spin up minecraft servers.
to spin up fabric server (set to 10G of ram usage, for lots of mods):
(bash)
sudo docker build -t fabmc1.21.4 .
sudo docker run -it -p 22222:25565 -v minecraft:/home --name yourfabricserver fabmc1.21.4

to spin up allthemods server:
