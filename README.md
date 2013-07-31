Shuttle
==================

Shuttle For Ubuntu is super simple & quick way to SSH into hosts defined in your *~/.ssh/config* file, and it does not comes in your way. You can still enjoy the command line pleasure that comes with ssh-config seamlessly.

Refer to the [Github page](http://ashisha.github.io/shuttle) to see what it looks like


Installing Shuttle
==================
Installing Shuttle is easy, fire up your terminal, and execute the following commands in order:

```Shell
sudo wget https://raw.github.com/ashisha/shuttle/master/shuttle -O /usr/bin/shuttle
sudo chmod +x /usr/bin/shuttle
mkdir -p ~/.config/autostart
sudo wget https://github.com/ashisha/shuttle/raw/master/shuttle.desktop -O ~/.config/autostart/shuttle.desktop
nohup shuttle >/dev/null &
```


Configuring Shuttle
===================
* Shuttle needs no configuration to run as such
* All the hosts listed in your *~/.ssh/config* will be automatically picked by Shuttle
* To prettify, **create groups** of your hosts by adding comments to your ssh config file as:
      ```#Shuttle Group <group>/<host description>```
* You can also **ignore** certain Host entries so as they do not appear in the Shuttle by adding an ignore comment as:
      ```#Shuttle Ignore```
* An example ssh config file may look like:

```Shell
    #Shuttle Group Work/Work 1
    Host pdc1
    Hostname 1.2.3.4
    
    #Shuttle Group WithoutGroup
    Host pdc2
    Hostname 1.2.3.5
    
    #Shuttle Ignore
    Host xlabs
    Hostname supersecret.example.com
```
* Refer the [Github page](http://ashisha.github.io/shuttle) for a WYSIWYG perspective
