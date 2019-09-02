Protostar
----------

Solutions to all Protostar exercises done using `pwntools`.

How I have setup the exercise?
==============================

I decided to isolate the VM network from the host machine, give
the VM a static IP from the root shell in order to prevent taining 
the disk image. 


On the host machine.

~~~bash
$ sudo brctl addbr protostar
$ sudo ip addr add 192.168.100.1/30 dev protostar
$ sudo ip link set dev protostar up
~~~

On the protostar VM

~~~bash
# ip addr add 192.168.100.2/30 dev eth0
# ip route add default via 192.168.100.1 dev eth0
~~~

Now you should be able to run the protostar exerises and exploits locally
too.