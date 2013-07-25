Shuttle
==================

Shuttle For Ubuntu is super simple & quick way to SSH into hosts defined in your *~/.ssh/config* file, without coming into your way. You can still enjoy the command line pleasure that comes with ssh-config.

Refer to the Github Page to see what it looks like.


Installing Shuttle
==================
Installing Shuttle is easy, execute the following commandsin order:

```mv shuttle.py /etc/init.d/```

```sudo chmod +x /etc/init.d/shuttle.py ```

```sudo update-rc.d shuttle.py defaults```



Configuring Shuttle
===================
* Shuttle needs no configuration to run as such
* All the hosts listed in your *~/.ssh/config* will be automatically picked by Shuttle
* To prettify, create groups of your hosts by adding comments to your ssh config file as:
      ```#Shuttle Group <group>/<host description>```
* An example ssh config file may look like:

```Shell
    #Shuttle Group Work/Work 1
    Host pdc1
    Hostname 1.2.3.4
    
    #Shuttle Group WithoutGroup
    Host pdc2
    Hostname 1.2.3.5
```

