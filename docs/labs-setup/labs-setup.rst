Labs setup/access
=================

In this section, we will cover our setup: 

* 1 basic cluster: 

	* 1 master (no master HA)
	* 2 nodes


We will connect to a pre-built environment in Ravello

In the existing environment, here is the setup you'll get: 

==================  ====================  ============  =============================================
     Hostname           Kubernetes IP          Role                 Login/Password
==================  ====================  ============  =============================================
     ip-10-1-1-4          10.1.10.11          Master        ssh: ubuntu/ravello - su : root/default           
     ip-10-1-1-5          10.1.10.21           node1        ssh: ubuntu/ravello - su : root/default
     ip-10-1-1-6          10.1.10.22           node2        ssh: ubuntu/ravello - su : root/default
     Windows              <public IP>        Jumpbox        rdp: student/agility
==================  ====================  ============  =============================================


Here are the different aspects to take into account during this installation guide: 

* We use *Ubuntu xenial* in the blueprints
* We updated on all the nodes the /etc/hosts file so that each node is reachable via its name

::

	#master and nodes host file
	$ cat /etc/hosts
	127.0.0.1       localhost
	10.1.10.11       ip-10-1-1-4 master1 master1.my-lab
	10.1.10.21       ip-10-1-1-5 node1  node1.my-lab
	10.1.10.22       ip-10-1-1-6 node2  node2.my-lab


You have many manuals available to explain how to install Kubernetes. If you don't use Ubuntu, you can reference to this page to find the appropriate guide:  `Getting started guides - bare metal  <http://kubernetes.io/docs/getting-started-guides/#bare-metal>`_ 

Here you'll find guides for:

* fedora
* Centos
* Ubuntu
* CoreOS
  
  and some other guides for non bare metal deployment (AWS, Google Compute Engine, Rackspace, ...)


