#READMEFILE
# These are my notes from the CELL class on SDN
# I created a github account on 4/7/2017 @ 03:23 hrs in order to learn more about code and the code way. 
# This file was upladed as a guild and a test. 
#
# Hello World - amazing



eth0 192.168.56.101
    To start OpenDaylight Hydrogen:

i. Run OpenDaylight from the OpenDaylight directory 
mininet@mininet-vm:~/opendaylight$ sudo ./run.sh -virt ovsdb
sudo ./run.sh -virt ovsdb
http://192.168.56.101:8080
http://<host only ip-address-of-machine-where-you-ran-opendaylight>:8080

2. To start mininet for the OpenFlow 1.0 simulation, use:
$ sudo mn --controller=remote,ip=127.0.0.1,port=6633
3. Mininet network should appear in Nodes Learned section.
Note: only one switch will appear, since the default mininet network has only 1 switch
You can view the Topology if you create a more complex network- 

sudo mn --controller=remote,ip=127.0.0.1,port=6633 --topo tree,3
sudo mn --topo=single,4
sudo mn --controller=remote,ip=127.0.0.1,port=6633 --topo=linear,4,4



@#@#@#@#@#@#@#@#
POX currently communicates with OpenFlow 1.0 switches and includes
special support for the Open vSwitch/Nicira extensions.

pox.py boots up POX. It takes a list of module names on the command line,
locates the modules, calls their launch() function (if it exists), and
then transitions to the "up" state.

Modules are looked for everywhere that Python normally looks, plus the
"pox" and "ext" directories.  Thus, you can do the following:

  ./pox.py forwarding.l2_learning

You can pass options to the modules by specifying options after the module
name.  These are passed to the module's launch() funcion.  For example,
to set the address or port of the controller, invoke as follows:

  ./pox.py openflow.of_01 --address=10.1.1.1 --port=6634

pox.py also supports a few command line options of its own which should
be given first:
 --verbose      print stack traces for initialization exceptions
 --no-openflow  don't start the openflow module automatically
 
 
 
 
 
 
# Initializing the FirewallTable
self.firewall = {}
# Adding sample firewall rules
self.AddRule(’00-00-00-00-00-01’,EthAddr(’00:00:00:00:00:01’))
self.AddRule(’00-00-00-00-00-01’,EthAddr(’00:00:00:00:00:03’))
    # Check the firewall Rules
    If self.CheckRule(dpidstr, packet.src) == False:
       drop()
       return
       
       
       
