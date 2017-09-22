# PAASMER Node

## What is Node-RED?
**Node-RED** is a programming tool for wiring together hardware devices, APIs and online services in new and interesting ways. It provides a browser-based editor that makes it easy to wire together flows using the wide range of nodes in the palette that can be deployed to its runtime in a single-click.

## Why Node-RED?
**Node-RED** is a visual tool for wiring the Internet of Things, but it can also be used for other types of applications to quickly assemble flows of services. It provides an easy setup and simple UI based on which we can create our own flows, wiring, programs, and share and save data. It is very intuitive and easy to use and needs very little programming experience as such. 

## What else can Node-RED do?
**Node-RED** can not only be used for Internet of Things applications, but it is a generic event-processing engine. For example you can use it to listen to events from http, websockets, tcp, Twitter and more and store this data in databases without having to program much if at all. You can also use it for example to implement simple **REST APIs**. 

## Pre-Requisites:
* Account in dashboard.paasmer.co.
* Raspberry PI 3 running Raspbian Jessie.
* Sensors and necessary wiring.

## Paasmer Nodes for Node-RED:
* The **Paasmer Nodes** for **Node-RED** are created for allowing configuration, connectivity, sensor data sharing and control of sensors from Node-RED or the Paasmer IoT platform. The Paasmer Nodes are written in **Node.JS** and are available as the npm repositories. 

* To install the Paasmer Nodes, Please execute the commands below.
#### Note: Please ensure that the Pre-requisites are all met before proceeding with installing the Paasmer Nodes.

## Install NodeJS :
Follow these commands to Install NodeJS Package in you system.
```
$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ sudo apt-get install -y build-essential
$ sudo apt-get update
```

## Install Node-Red
```
$ sudo npm install -g --unsafe-perm node-red
```

## Start Node-Red
```
$ node-red (or)
$ node-red-start //Raspberry Devices
```

## Install Paasmer Nodes
You can choose to install Paasmer Nodes using the command line in root directory of node-red installation (or)Search `paasmer` keyword in node-red `options` => `Manage Palette` => `Install` Tab
```
$ npm install node-red-contrib-paasmer 
```

## Paasmer Config Node:
* This node requires Paasmer login information, device information and feeds configuration. 
* You have to configure the node details and click “Done”

 ![image](https://github.com/PaasmerIoT/Paasmer-Node/blob/master/Images/Paasmer_config.png?raw=true)

## Paasmer Out & Paasmer In Nodes:-
* These are the nodes that interact with your feeds. Paasmer Out node will send sensor data to Paasmer platform and Paasmer In node helps to control your actuators.
* To configure nodes, select anyone of the node and create a device connection, and click Update and then click on done. Select the same connection to other node also.
 
### Paasmer In Node
 ![image](https://github.com/PaasmerIoT/Paasmer-Node/blob/master/Images/Paasmer_In.png?raw=true)
### Paasmer Out Node
![image](https://github.com/PaasmerIoT/Paasmer-Node/blob/master/Images/Paasmer_Out.png?raw=true)

#### Wiring
* Connect Paasmer-config output to Paasmer-out node (choose from palette) and input to Inject Node at an interval.
* Connect Paasmer-out node input to Paasmer-config out node.
* Connect Paasmer-in node output to Debug node, and check feed controlling data.
![image](https://github.com/PaasmerIoT/Paasmer-Node/blob/master/Images/Paasmer_Wiring.png?raw=true)
 
