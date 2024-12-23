# docker4minecraft
This is my collection of dockerfiles to spin up minecraft servers.
to spin up fabric server (set to 10G of ram usage, for lots of mods):
(bash)
sudo docker build -t yourfabricserverimagename .
sudo docker run -it -p preferred_host_port:25565 -v namedvolumeforpersistence:/home --name PleaseNameYourContainer yourfabricserverimagename

to spin up allthemods server:
sudo docker build -t yourATM10serverimagename .
sudo docker run -it -p preferred_host_port:25565 -v namedvolumeforpersistence:/home --name pleasenameyourContainer yourATM10server
