This example illustrates RPC in Python using the RPyC library (https://rpyc.readthedocs.io/).

It consists of a server that exposes two remotely accessible procedures used to manipulate a list:

- value(): returns the current value of the list (its elements)
- append(): adds a new element to the end of the list

### Before running the example, you need to install the RPyC library:

Do the following on two different machines (AWS EC2 instances)

    sudo apt update
    sudo apt install python3-rpyc

### Then edit the constRPYC.py file to use the IP address of the machine where you will run the server:

Also make sure it is using one of the ports left open for incoming TCP connections on the firewall (security group), such as 5678

### Then run the server on one machine

    python3 server.py

(and leave it running)

### Then run the client on the other machine

    python3 client.py

### Now add other remote procedures to the server and change the client to test them

You may add the same remote procedures that you added in the sockets activity.
