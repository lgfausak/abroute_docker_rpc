# abroute_docker_adm - adm script for this group

## Overview

adm, this is simply the admin utility, like adding topics or users or roles. monitoring activity. etc.

Autobahn provides for registering functions with a name, and calling them remotely as well
as publish / subscribe functionality. This code is based upon the concept
that the names that are registered with Autobahn (topics) are logical domains. They
are dot separated subjects.  E.g. com is the logical parent of com.devices which in
turn is the logical parent of com.devices.fan.  Using this heirchy, We can map permissions
on top to control the actions we can take on the topic. The actions that can be controlled are
* register - register a function
* call - call an already registered function
* publish - publish a message to a topic
* subscribe - subscribe to a topic channel
* admin - grant these actions / permissions to others

## Docker Container Layout

![alt text][docker_containers]

[docker_containers]:https://github.com/lgfausak/sqlauth/raw/master/docs/docker_containers.png "Docker Containers"
