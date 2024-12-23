# docker4minecraft
This is my (small) collection of dockerfiles to spin up minecraft servers.

# to spin up fabric server 
(set to 10G of ram usage, for lots of mods. you can edit the dockerfile's entrypoint to change):


(bash)

sudo docker build -t yourfabricserverimagename .

sudo docker run -it -p preferred_host_port:25565 -v namedvolumeforpersistence:/home --name PleaseNameYourContainer yourfabricserverimagename

use -it to keep it interactive for future sessions. you can quit out after first run and start it with docker start containername

# to add your mods:


sudo docker ps (lists your containers)

sudo docker cp /path/to/mods/folder 02ae(containerID)ff32:/home/

if your mods aren't in a mods folder or you are adding individually, then do docker cp path/to/mod/mod.jar containerID:/home/mods

# to spin up allthemods server:


sudo docker build -t yourATM10serverimagename .

sudo docker run -it -p preferred_host_port:25565 -v namedvolumeforpersistence:/home --name pleasenameyourContainer yourATM10serverimagename

If there is a newer version of neoforge used and I didn't update the script, let me know via issues and I will.
This is based on 12/22/24's 21.1.90 neoforge release; but it will pull updates from their github and unless the neoforge 
version changes everything should work out fine.
# you are responsible to copy the mods in from ATM-10! 
